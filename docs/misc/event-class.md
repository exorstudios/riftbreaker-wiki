---
layout: default
title: Event class
parent: Misc
nav_order: 3
---

# Information

When working with events, the event class is used to access event information.  
It can't be used any other way.  


# Functions
  
Not every event function works for every event type.  
It's recommended to use the game reflection tool in the workspace editor to get more information about it. 
  

```qml
evt:GetBlueprint()
evt:GetControlledEntity()
evt:GetContinous()
evt:GetCreator()
evt:GetCubeEnt()
evt:GetDatabase()
evt:GetDamageType()
evt:GetDamageValue()
evt:GetDamagePercentage()
evt:GetDegree()
evt:GetDeltaTime()
evt:GetEffect()
evt:GetEmissiveValue()
evt:GetEntity()
evt:GetEvent()
evt:GetForced()
evt:GetFullExit()
evt:GetGrowSpeed()
evt:GetOtherEntity()
evt:GetOwner()
evt:GetPlayerId()
evt:GetPrepareBlueprint()
evt:GetItem()
evt:GetItemEnt()
evt:GetInventory()
evt:GetLeechDamage()
evt:GetMarkerName()
evt:GetMenu()
evt:GetMode()
evt:GetNewStateName()
evt:GetReason()
evt:GetResource()
evt:GetShootBlueprint()
evt:GetSlot()
evt:GetTarget()
evt:GetTargetTag()
evt:GetTeam()
evt:GetTime()
evt:GetTurretEntity()
evt:GetTurretStatus()
evt:GetUpgrading()
evt:GetVisible()
```

## Example

```qml
function tower:OnResourceMissingEvent( evt )
	local resource = evt:GetResource()
	if ( resource ~= "energy" and resource ~= "ai" and ConsoleService:GetConfig("g_tower_ammo_missing_annoucements") == "1" ) then
		EntityService:ShowTimeoutSoundEvent( INVALID_ID, 30.0, "voice_over/announcement/not_enough_ammo_tower", false )
	end
end
```