---
layout: default
title: Structure of Lua files 
nav_order: 1
parent: Lua files
grand_parent: Modding files
---

# Information

LUA files, regardless of whether they are for buildings, units, etc., always have the same structure.

# Example file - Morphium Tower

Let's take the following file as an example, the lua file for the morphium tower, `tower_alien_influence.lua`

{% capture some_var %}
{% highlight lua linenos %}
local tower = require("lua/buildings/defense/tower.lua")
require("lua/utils/table_utils.lua")

class 'tower_alien_influence' ( tower )

function tower_alien_influence:__init()
	tower.__init(self,self)
end

function tower_alien_influence:OnInit()
    tower.OnInit(self)

    self.cfsm = self:CreateStateMachine()
    self.cfsm:AddState( "checker", { execute="OnExecuteChecker", interval=1.0 } )
    self.cfsm:ChangeState("checker")
    self.created = false

    self.active = true
	self.selected = {}
    self.radius = self.data:GetFloatOrDefault("radius", 6)
	self.interval = self.data:GetFloatOrDefault("interval", 1)
	self.shieldBp = self.data:GetStringOrDefault("shield_bp", "buildings/defense/shield_generator/shield")
	self.healthChild = INVALID_ID

    self.fsm = self:CreateStateMachine()
	self.fsm:AddState( "working", {execute="OnWorkInProgress",exit="OnWorkExit", interval=self.interval} )

	self:RegisterHandler( self.entity, "SpikeAmmoFiredEvent",  "OnSpikeAmmoFiredEvent" )
end

function tower_alien_influence:OnSpikeAmmoFiredEvent( evt )
	AnimationService:StartAnim( self.entity, "working", false )
end

function tower_alien_influence:OnExecuteChecker( state )
    if (self.working == self.created ) then
        return
    end

    if ( self.working ) then
		local workingTime = BuildingService:GetWorkingTime( self.entity )
        if ( workingTime and workingTime > 1.0 ) then
            local influenceComponent =EntityService:CreateComponent(self.entity, "InfluenceComponent")
            local influenceComponentHelper = reflection_helper(influenceComponent)
            influenceComponentHelper.radius = 13
            influenceComponentHelper.energy_radius = 0
            influenceComponentHelper.emissive_radius = 5
            self.created = true
        end
    else
	    EntityService:RemoveComponent(self.entity, "InfluenceComponent")
        self.created = false
    end

end

function tower_alien_influence:OnWorkInProgress( state )
	if ( self.healthChild == INVALID_ID or HealthService:GetHealth( self.healthChild)== -1 ) then
		self.healthChild = EntityService:SpawnAndAttachEntity( self.shieldBp, self.entity )
		return
	end
	local objects = FindService:FindEntitiesByTypeInRadius( self.entity, "building", self.radius )
			
	for i = 1, #objects do			
		if( IndexOf( self.selected, objects[i] ) == nil and BuildingService:IsBuildingFinished( objects[i] ) )
		then
			ItemService:AddHealthLink( objects[i], self.healthChild )
			Insert( self.selected, objects[i] )	
		end
	end		
	
	for i = #self.selected,1,-1  do			
		if( IndexOf( objects, self.selected[i] ) == nil ) then
			ItemService:RemoveHealthLink( self.selected[i], self.healthChild )
			Remove( self.selected, self.selected[i] )	
		end
	end		
end

function tower_alien_influence:OnWorkExit( state )
	for i = #self.selected,1,-1  do		
		ItemService:RemoveHealthLink( self.selected[i], self.healthChild )
	end		
	Clear( self.selected )
end


function tower_alien_influence:OnActivate()
	self.fsm:ChangeState("working")
end

function tower_alien_influence:OnDeactivate()
	local state = self.fsm:GetState("working")
	if ( state ~= nil ) then
		state:Exit()
	end	 
end

return tower_alien_influence

{% endhighlight %}
{% endcapture %}
{% include fix_linenos.html code=some_var %}

# Explanation

| Line        | Explanation     |
|:-------------:|--------------|
| 1-2 |  	Dependencies - The code in this lua depends on those files. Line 1 is needed since the morphium tower is a tower and requires the normal tower functions as a base to start on. Line 2 is needed for code inside this file, so the code knows how to work with code based tables.    |
| 4 | Defines the class of this file  |
| 6 - 8  | A function for the very first initialization of the tower backend. Does nothing else than initialize the general tower.lua defined in line 1  |
| 10 - 29 | The first initialization of this actual tower. The function gets executed as soon as the player clicks a spot on the map and the tower would get build. Timeframe between the player clicking to build and the drones building the tower. Used to create StateMachine for states, RegisterHandlers for events.   |
| 30 - 97 | Every other function created in this file. Always follows the principle of `function name_of_the_file:Name_of_the_function`. You might also use the StateMachine to create functions with states or use events created with the RegisterHandler. |
| 99  | The end of the file. Is required to actually return information from inside this LUA to the game. |