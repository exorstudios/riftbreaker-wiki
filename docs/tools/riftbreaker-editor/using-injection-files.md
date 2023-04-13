---
layout: default
title: Using injection files 
nav_order: 2
parent: Riftbreaker editor
grand_parent: Tools
---

# Injection files
Sometimes you want to modify files which are either very long or are often changed by the developers so you have to re-edit them after every patch to keep up with the game version.  
Read all about them here: [Modifying original files by creating injection files](../../../modding-files/dat-files/modifying-original-files-by-creating-injection-files)

# Using injection files with the riftbreaker-editor
# Weapon_stats
Create an **empty** weapon_stats.dat injection file, like `aoe_weapon_stats.dat`:
![](../../../../assets/images/using-injection-files_1.png){: width="600px"}  

Top left, use "File -> Open -> File...":
![](../../../../assets/images/using-injection-files_2.png){: width="600px"}  

Choose your `_weapon_stats.dat` file:
![](../../../../assets/images/using-injection-files_3.png){: width="600px"}  

A popup will appear which shows that new entities have been found and should be added to the injection file, click Yes:
![](../../../../assets/images/using-injection-files_4.png){: width="600px"}  

Work around in that file using the Riftbreaker Editor and save it.
Afterwards, the tools will automatically create a `_weapon_charge_factors.dat` file and fill the `_weapon_stats.dat` file with the required information:
![](../../../../assets/images/using-injection-files_5.png){: width="600px"}  
