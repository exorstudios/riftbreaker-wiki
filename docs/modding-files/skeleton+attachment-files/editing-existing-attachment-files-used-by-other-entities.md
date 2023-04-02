---
layout: default
title: Editing existing attachment files used by other entities 
nav_order: 1
parent: Skeleton + Attachment files
grand_parent: Modding files
---

# Information
If you want to edit existing attachment files, f.e by using it for another building, you have to do it in 3 steps:  

1. Copy the existing `.skeleton` and `.att` file to your mod
2. Rename them both to something fitting to your mod. Example: "my_mod.skeleton" + "my_mod.att". Both have to use the same name
3. Change the SkeletonDesc in the blueprint of your modded entity to f.e `meshes/buildings/defense/my_mod`. **No file extension**  

The game associates the attachment file together with the skeleton file.   
That's why you have to rename the ".skeleton" and ".att" file to the same name.  
Like this, the game will use the information from the SkeletonDesc to search for the att file with the same name. 