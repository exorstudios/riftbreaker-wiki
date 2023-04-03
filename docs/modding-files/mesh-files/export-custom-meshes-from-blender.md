---
layout: default
title: Export custom meshes from Blender
nav_order: 2
parent: Mesh files
grand_parent: Modding files
---

Use the EXOR mesh exporter with Blender version 3.1.2 at max! 
{: .warning}

# Final check
Check the following for each of the available meshes you want to export:  
1. Clean, real name (for collision boxes, have the "_cX" suffix)  
2. Triangulated  
3. All transforms normalized  

# The export
Select every mesh you want to export and go to `File -> Export -> EXOR Mesh`  
(If you have an armature for bones, select it too)  
![](../../../../assets/images/mesh-files_export_custom_meshes_from_blender.png)  
In the exporter menu, leave everything as it is ( you might want to try around with the checkboxes at the top "Selected Objects" + "Active Collection" ), make sure the transform is set as in the picture below.  
![](../../../../assets/images/mesh-files_export_custom_meshes_from_blender_2.png)  
Once this is finished, you will find your exported file(s) in your filesystem.  
![](../../../../assets/images/mesh-files_export_custom_meshes_from_blender_3.png)  

# Quick check
For a quick check without too much hassle and details, you can download Ogre Meshy to view the mesh files.  

# Common errors
- The EXOR exporter uses the name of the mesh in the scene collection as the name of the mesh file in the filesystem, **not** the name of the Blender save file.  
- If you use the default EXOR mesh exporter settings, make sure to have every mesh in your collection selected you want to export - see the EXOR exporter setting "Selected Objects"