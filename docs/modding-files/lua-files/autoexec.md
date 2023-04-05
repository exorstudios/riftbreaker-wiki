---
layout: default
title: Autoexec
nav_order: 2
parent: Lua files
grand_parent: Modding files
---

# Information
Autoexec files are files which get executed on map creation.  
It allows access to all services + reflection + RegisterGlobalEventHandler to create a "master" script with global hooks.

# Requirements
- Lua files which end with " _autoexec.lua" in the Lua folder

# RegisterGlobalEventHandler
Since the _autoexec file is not an LuaEntityObject, we can't access things like the RegisterHandler and StateMachine.  
To solve this, the _autoexec file can use the RegisterGlobalEventHandler.  
It listens for **all** events, like an event_sink, and can access that information.  
Like that, it's a nice way to unlock something on a global level.

## Example
A simple example how to unlock a building as soon as the player mech is created (=spawned for the first time). Like this, no research is required.

```lua
RegisterGlobalEventHandler("PlayerCreatedEvent", function(arg)
    BuildingService:UnlockBuilding("Path/to/Blueprint")
end)
```