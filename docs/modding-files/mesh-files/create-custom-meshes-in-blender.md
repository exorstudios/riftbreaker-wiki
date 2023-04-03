---
layout: default
title: Create custom meshes in Blender
nav_order: 1
parent: Mesh files
grand_parent: Modding files
---

Use the EXOR mesh exporter with Blender version 3.1.2 at max! 
{: .warning}

# Information
Get the EXOR mesh exporter [here](https://github.com/exorstudios/riftbreaker-tools/tree/main/exor_exporters/plugins/exor_mesh_exporter)  
The Readme.txt has the necessary instructions how to install the plugin.

# Mesh creation
his following step-by-step tutorial is kept simple just to have a simple beginner path which can then be used for more difficult projects. 
## Scaling
Each building grid tile in The Riftbreaker is 2x2 meters - by default the Blender grid has 0.5x0.5 meter tiles.
So a 1x1 building grid in The Riftbreaker = 2x2 Blender grid tiles OR 1x1 on the Blender scale.  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender.png)  

## Create your object
At first, you need to create something, in this example I use a simple Blender greybox as a single cube mesh which I scaled up to 2x2x1 (scale) in size and set the Z-location to 1, so it's standing on the ground.  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender_2.png)  

## Triangulate your meshes
For every mesh you might have created for this object, you need to triangulate it.  
To do so, select every mesh and choose the modifier properties side menu.  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender_3.png)  
In here, add another modifier, called "Triangulate".  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender_4.png)  
Once added, you can see it as a modifier in the open menu and at the top as a small wrench icon next to the mesh where you added it.  
No need to extra apply anything, just like in the picture below is ok.  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender_5.png)  

## Normalize all transforms
As the final step, you have to normalize all transforms so The Riftbreaker can work with the scaling.  
To do this, select all relevant meshes and press "ctrl + a" and click "All Transforms".  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender_6.png)  
Once you have done that, your current model transforms will be set as the new "default" / "normal".  
It still has the changed values for location, scale etc, but the values are now back to default.  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender_7.png)  

## Clean up mesh names
Once you have a finished mesh you wish to use in the game The Riftbreaker, edit all the mesh names, so they get a real name - the name of the mesh will become the name of the mesh file in the filesystem.  
To change those names, select the meshes and either change the bottom textbox, or select it in the top list and press F2 to rename it.  
![](../../../../assets/images/mesh-files_create_custom_meshes_in_blender_8.png)  

# Common errors
- A Blender scale of 1.0 doesn't mean 1 blender grid block, but 1 meter in length.  

# External source
[https://store.steampowered.com/news/app/780310/view/5375631932961299786](https://store.steampowered.com/news/app/780310/view/5375631932961299786)