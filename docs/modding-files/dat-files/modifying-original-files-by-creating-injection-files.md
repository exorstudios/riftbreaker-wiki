---
layout: default
title: Modifying original files by creating injection files 
nav_order: 1
has_children: true
parent: Dat files
grand_parent: Modding files
---

# Information

Sometimes you want to modify files which are either very long or are often changed by the developers so you have to re-edit them after every patch to keep up with the game version.  
For this case, the developers added an option to create injection files which are automatically added to the original files they belong to.  
**Example:** The file `weapon_stats.dat` keeps a lot of information.  
It would be tedious to keep up with updating it every patch.  
Instead you create `XYZ_weapon_stats.dat` where you add your new stuff. 
  
# Requirements
  
- Only works for script files
- The file you create has to have the original file name in its name.  
Original file name: `weapon_stats.dat`, injection file name: `XYZ_weapon_stats.dat`.  
Where XYZ can be whatever you want, like the name of the mod you are creating. 
  
# Supported paths
  
Not every path allows for injection files, the supported paths are:  
- `scripts\blueprint_tables\*` (not vegetation_lifecycle.dat)  
- `scripts\buildings\*`  
- `scripts\debug\*`  
- `scripts\hud\*`  
- `scripts\units\*`