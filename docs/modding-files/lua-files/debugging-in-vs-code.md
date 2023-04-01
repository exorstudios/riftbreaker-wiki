---
layout: default
title: Lua debugging in Visual Studio Code
nav_order: 99
parent: Lua files
grand_parent: Modding files
---
{: .warning}
You can only attach to Lua state when The Riftbreaker in active map gameplay or loading into one

# Information

How to enable LUA debugging in Visual Studio Code

# Installation

1. Install VSCode: https://code.visualstudio.com/
2. In VSCode, install the LRDB (Lua Remote DeBugger) extension

# Configuration

1. Create a developer.cfg file in your Riftbreaker documents directory  
"\Documents\The Riftbreaker\config"
2. Add `set debug_lua 1` into your newly created developer.cfg file
3. Use the open folder feature of Visual Studio Code and open your mod directory
4. Use the Visual Studio Code Debugger tab and click the small text saying "Create launch.json file"
5. Replace all contents of `launch.json` with:
```qml
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "type": "lrdb",
            "request": "attach",
            "host": "localhost",
            "port": 21110,
            "name": "The Riftbreaker - Attach",
            "sourceRoot": "${workspaceFolder}"
        }
    ]
}
```

# Using the debugger

1. Launch game and any map 
2. Setup breakpoints wherever you want and press F5 or "Start debugging" button in the Debugger tab