---
layout: default
title: Lua debugging using Lua services
nav_order: 98
parent: Lua files
grand_parent: Modding files
---

# Information

The easiest & quickest way to debug Lua actions is using integrated Lua services provided by EXOR themselves.

# Using logs

The Riftbreaker uses log files to log actions happening inside the game. Those logs can be found in **\Users\[NAME]\Documents\The Riftbreaker\exor_logs.txt**.  
It has 6 log files, from "exor_logs.txt" to "exor_logs.5.txt" even though only 1 gets used at a time, every other file is older.  
To use this file, you can use the Lua-Service called **LogService** inside the Lua files you want to check. 

## Logs example

```lua
LogService:Log("Option 1")
```
When this part gets executed inside the Lua file, the exor_logs.txt would show an entry where it would say the name of the Lua file and whatever it should log.

# In game

For a quicker way (in case the game doesn't crash) and the option to see a log entry in game, you can use the Lua-Service called **ConsoleService** 

## In game example

```lua
ConsoleService:Write("Option 1")
```
When this part gets executed inside the Lua file, whatever is written inside the ( ) gets written directly to the in game console.  