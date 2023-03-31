---
layout: default
title: DDS files 
nav_order: 1
has_children: true
parent: Gui + Texture files
grand_parent: Modding files
---

{: .warning }
View page [Material requirements](../material-requirements) before attempting custom graphics

# Information

A DDS file is an image saved in a so called "DirectDraw Surface (DDS)" container format.  
Riftbreaker uses it, as it's supported by GPU hardware and is stored in a compressed state inside video memory.  

# Requirements
## Encoding

- RGBA8/R8G8B8A8
- ABGR8  

Any other encoding type will likely cause the game to crash on startup.  

## Compression

- uncompressed / none
- BC2 / DTX3
- BC3 / DTX5  
  
# Creation / Editing recommendation
  
If you plan to create/modify such files, try testing out either GIMP or paint.net as they are able to save a DDS file in many different DDS compressions.  
Paint.net also offers things like saturation tool and temperature tool which helps creating / modifying files.