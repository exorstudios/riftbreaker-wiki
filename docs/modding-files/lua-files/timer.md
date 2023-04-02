---
layout: default
title: Timer
nav_order: 94
parent: Lua files
grand_parent: Modding files
---

# Information
The following code allows using simple timers in Lua scripts 

# Code
```qml
function timer_based_unit:OnTimerElapsedEvent( evt )
    local handler = self[evt:GetName()]
    handler(self)
end

function timer_based_unit:RequestTimerCallback( function_name, timeout)
    -- Ensure entity has TimerComponent
    EntityService:CreateComponent( self.entity, "TimerComponent")
    QueueEvent( "SetTimerRequest", self.entity, function_name, timeout )
end

function timer_based_unit:OnInit()
    self:RegisterHandler( self.entity, "TimerElapsedEvent", "OnTimerElapsedEvent")

    self:RequestTimerCallback("SpawnUnits", 10.0)
    self:RequestTimerCallback("DoRandomStuff", 3.0)
end

function timer_based_unit:DoRandomStuff()
    -- do stuff
end

function timer_based_unit:SpawnUnits()
    -- do stuff
end
```