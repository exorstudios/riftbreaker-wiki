---
layout: default
title: Override used mesh material 
nav_order: 99
parent: Mesh files
grand_parent: Modding files
---

# Information
Sometimes, especially in older meshes used by X-Morph, the material is baked directly into the mesh file. How to solve this problem when trying to use a different material is listed here. 

# Find the baked material name
Open the *.mesh file with a desired Hex-Editor or even Notepad, and search for a fitting name, example:  
![](../../../../assets/images/mesh-files_override_mesh.png)  
Which shows "projectiles/railgun_projectile_beam" as text.  
  
# Override used material
You can override used material by just adding a "material" field to MeshDesc of the entity file:  
![](../../../../assets/images/mesh-files_override_mesh_2.png)  
