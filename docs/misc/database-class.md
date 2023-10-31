---
layout: default
title: Database class
parent: Misc
nav_order: 2
---

# Information

For certain actions, it's required to access the database class which offers many different functions to use.

# Functions
  
Below, a functions overview.  
In this case, the variable for the database is called `my_database`, that's why it starts with `my_database`  
  
{: .highlight }
To create a database use:<br/> local my_database = PlayerService:GetOrCreateGlobalDatabase('name_of_database')"  
  

```qml
my_database:HasString("biome_requirement")
my_database:SetString("alpha", "beta" )
my_database:GetString("biome_requirement")
my_database:GetStringOrDefault( "display_radius_group", tostring(self.entity) )

my_database:HasFloat("damage_resisted_stun_speed")
my_database:SetFloat("drone_search_radius", 10 )
my_database:GetFloat("damage_resisted_stun_speed")
my_database:GetFloatOrDefault("drone_search_radius", 25.0)

my_database:HasInt("drone_id")
my_database:SetInt("drone_id", 3 )
my_database:GetInt("drone_id")
my_database:GetIntOrDefault( "drone_per_spot", 2 )

my_database:HasVector(????)
my_database:SetVector(????, ????)
my_database:GetVector(????)
my_database:GetVectorOrDefault(????, ????)

my_database:GetStringKeys()
my_database:GetFloatKeys()
my_database:GetIntKeys()
my_database:RemoveKey(????)

my_database:Clear() (Clears a database)
my_database:Empty() (Checks if a database is empty)
```

## Example

```lua
local my_database = PlayerService:GetOrCreateGlobalDatabase( "g_lvl_system_database")
my_database:SetInt( "xp", my_database:GetIntOrDefault("xp", 0) + 1)
```