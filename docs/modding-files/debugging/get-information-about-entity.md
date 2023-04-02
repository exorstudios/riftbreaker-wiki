---
layout: default
title: Get information about an entity 
nav_order: 1
parent: Debugging
grand_parent: Modding files
---

# Information
Sometimes it's necessary to do some live debugging in game and find some information about an entity. 

# Debugging
Open the console and type `debug_enitity_signature_picker`  
This will start the signature picker and you can move your mouse around the screen to find information about the entity you are hovering above.  
  

To filter the entities, you can use the components like `debug_enitity_signature_picker MeshComponent`  
So it only allows to pick entities with a mesh.    

As a result, you get a nice entity overview ingame: 
![](../../../../assets/images/debugging_entity_picker.png)  