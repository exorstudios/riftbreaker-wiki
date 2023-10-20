---
layout: default
title: Reflection helper
nav_order: 3
parent: Lua files
grand_parent: Modding files
---

# Information

The reflection helper is a powerful part of Lua coding, it helps to access values for GetField, GetValue, IsContainer and ToContainer. 

# Component vs SingletonComponent
## Component

Is a storage per local entity, each entity can have their own instance of some component.  
Lua:
```lua
EntityService:GetComponent(ENTITY, "COMPONENT")
```

## SingletonComponent

Is for global storage and is not tied to any entity, no matter in which place you call it you will get the same instance of the data.  
Lua:
```lua
EntityService:GetSingletonComponent("COMPONENT")
```

# Using the reflection helper

At the beginning of your lua file should be the require for the reflection element:
```lua
require("lua/utils/reflection.lua")
```

In your code, use the reflection helper in combination with components to access component values:
```lua
local refl_MechComponent = reflection_helper( EntityService:GetComponent(self.entity, "MechComponent"))
LogService:Log( tostring(refl_MechComponent)  )
```
If you need to go one "layer" deeper into the information, you can use [Dot Notation](https://en.wikipedia.org/wiki/Property_(programming)#Dot_notation) and just append what you need, for example:  
```lua
refl_MechComponent.zoom 
refl_MechComponent.velocity 
refl_MechComponent.pickup_radius
```

{: .highlight}
Use the game reflection to get an overview of available components and their properties
