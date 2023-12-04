---
layout: default
title: Survival mode
nav_order: 2
parent: game-flow
grand_parent: Topics
---

# Information

This page intends to kickstart the knowledge about the general game flow of the survival mode, based on the actual game files and tools.  
Many different files will be accessed as well as tools used. The flow will be kept short, as most information inside the files are often self-explanatory.  

# The structue

The basic structure of the survival mode is separated into 4 chunks:  
Setting files, Logic files, the DOM, Lua files  

## Various setting files  

The setting files set the actual flow of the files. These include f.e `.campaign` files, `.mission` files.  

## Logic files (Mission editor)  

Logic files can be accessed by the [Mission editor](../../../tools/mission-editor/mission-editor/) which shows the actual graph nodes of the things happening in that logic file.  
Each logic file is created to complete a particular task by using a graph flow of it happening.  

## The DOM (Dynamic Objective Manager)  

The actual attack waves are triggered by the DOM. It's like the game master of the actual survival match.  
It sets the wave difficulty, chooses a fitting wave and orders it to spawn at a chosen spawn point.  
It does **not** however, create the waves like an algorithm on the spot, but chooses a wave from a pool of pre-created logic files.  

## Lua files  

As usual, Lua tends to be the backbone of most stuff happening - the same applies here.  
The Lua files set the start of the logic files for a biome, the game diffituly rules for the DOM, warmup duration, mission duration, etc.  
It connects logic files and difficutly rules to the DOM as well as setting the guidelines of the survival match.  


# Flow overview

Now that the basic functionalities have been explained, we can list a flow of an exemplary survival match in the jungle biome
1. The game menu initiates the .campaign file e.g. `campaigns/survival/jungle.campaign` when selecting survival jungle
2. The campaign file contains the initial mission definition - in this case:  
`startup_mission_def          "survival/jungle"`
3. That file can be found as `missions/survival/jungle.mission`
4. In this file it points to the mission startup script:  
`script          "lua/missions/survival/survival_jungle.lua"`
5. Inside the `survival_jungle.lua` it activates the initial mission `.logic` file with
```lua
MissionService:ActivateMissionFlow("", "logic/missions/survival/default.logic", "default", database )
```
6. Inside the `survival_jungle.lua` it also sets the DOMs rules script with:
```lua
local rulesPath = GetRulesForDifficulty( "lua/missions/survival/v2/dom_survival_jungle_rules_" )
MissionService:AddGameRule( "lua/missions/v2/dom_manager.lua", rulesPath )
```
7. The mission flow of `logic/missions/survival/default.logic` activates the  
`logic/missions/survival/warmup.logic` file - it's just a bit of custom logic that didn't fit the DOM architecture
8. After the `warmup.logic` is complete, it activates the DOM which then handles the match waves
9. DOM starts by looking at the default dom rules file - other difficulty specific files derive from it and simply overload the data from the default script:  
\lua\missions\survival\v2\dom_survival_jungle_rules_default.lua`
10. After the survival time is over, the DOM is deactivated again and a custom final wave logic is triggered, as found in the `logic/missions/survival/default.logic`  
  
# default.logic
## Start
![](../../../../assets/images/game-flow_survival.png)

## END
![](../../../../assets/images/game-flow_survival_end.png)