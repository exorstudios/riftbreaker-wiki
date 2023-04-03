---
layout: default
title: Edit entity files to use custom meshes
nav_order: 4
parent: Mesh files
grand_parent: Modding files
---

# Information
To use your mesh files in the game, you need to associate them with entity files.  
This page covers the different things you have to pay attention to while creating or modifying an entity file.

# Mesh selection
## MeshDesc
The most important part of the entity file in regard to the mesh is the mesh selection, this is done by using the MeshDesc. In here you specify which mesh file and material shall be used.  
```qml
MeshDesc
{
    mesh        "meshes/props/special/alien_structures/Modding_Tutorial.mesh"
    material    "props/special/alien_structures/influence_pylon"
}
```

# Mesh shape
## GridCullerDesc
The GridCullerDesc is the part between the mesh file and the building grid of the Riftbreaker. It tells the game about the size of the mesh so it fits onto the building grid.  
You have 2 options to pick from, either use the collision mesh:  
```qml
GridCullerDesc
{
    Shapes
    {
        PhysicsMeshShape
        {
            mesh    "meshes/props/special/alien_structures/Modding_Tutorial_c1.nxs"
        }
    }
}
```  
or set it manually as a shape:  
```qml
GridCullerDesc
{
    Shapes
    {
        PhysicsBoxShape
        {
            x   2
            y   2
            z   2
        }
    }
}
```  
## PhysicsDesc
The PhysicsDesc describes the physics of the mesh, it depends on what you want the physics to be.  
Here you have different options to choose from, either use the collision mesh:  
```qml
PhysicsDesc
{
    objects
    {
        PhysicsObjectDesc
        {
            type                "static"
            group_id            "building"
            physics_material    "default"
            Shapes
            {
                PhysicsMeshShape
                {
                    mesh    "meshes/props/special/alien_structures/Modding_Tutorial_c1.nxs"
                }
            }
        }
    }
}
```  
or set it manually as a PhysicsCapsuleShape:  
```qml
PhysicsDesc
{
    objects
    {
        PhysicsObjectDesc
        {
            type                "static"
            group_id            "building"
            physics_material    "default"
            Shapes
            {
                PhysicsCapsuleShape
                {
                    r   "1.45"
                    half_height "2"

                    position
                    {
                        x   "0.0"
                        y   "2"
                        z   "0.0"
                    }

                    orientation
                    {
                        w   "0.7"
                        x   "0.0"
                        z   "0.7"
                        y   "0.0"
                    }
                }
            }
        }
    }
}
```  
or set it manually as a PhysicsBoxShape:  
```qml
PhysicsDesc
{
    objects
    {
        PhysicsObjectDesc
        {
            type                "static"
            group_id            "building_small"
            physics_material    "default"
            Shapes
            {
                PhysicsBoxShape
                {
                    x   "0.5"
                    y   "8"
                    z   "0.5"

                    position 
                    {
                        x   "0.0"
                        y   "4"
                        z   "0.0"
                    }
                }
            }
        }
    }
}
```  
or set it manually as a PhysicsSphereShape:  
```qml
PhysicsDesc
{
    objects
    {
        PhysicsObjectDesc
        {
            type                "static"
            group_id            "building"
            physics_material    "default"
            Shapes
            {
                PhysicsSphereShape
                {
                    r   "3.45"

                    position 
                    {
                        x   "0.0"
                        y   "1.0"
                        z   "0.0"
                    }
                }
            }
        }
    }
}
```  
For the value of `type` you can have strings like `static`, `dynamic`, `kinematic` etc etc.  

For the value of `group_id` you can have strings like `building`, `building_small`, `loot`, `vegetation`, `destructible`, `world`, `world_blocker`, `wreck`, `grenade`, `ground_unit`, `floor` etc etc.  

For the value of `physics_material` you can have strings like `default`, `gibs_light`, `grenade_light` etc etc.  

All these values might change something, but it's unknown yet what exactly. So be sure to look at similar entity files for what you are trying to create and take a look.  

## LuaDesc
The LuaDesc isn't really important for the mesh shape, but has one exception, the cone effect.  
So when you have a basic Lua, you have to add `cone_effect` and `cone_effect_sell` to be fitting for your building.  
```qml
LuaDesc
{
    script  "lua/buildings/building.lua"

    database
    {
        cone_effect         string:"build_cone_3x3"
        cone_effect_sell    string:"sell_big"
    }
}
```  
<table>
    <tr>
        <th>Name</th>
        <td>Description</td><td>Examples</td>
    </tr>
    <tr>
        <th>cone_effect</th>
        <td>Defines how big the scaffolding should be when the building is being build</td><td>string:"build_cone_3x3", string:"build_cone_1x1", string:"build_cone_6x7", string:"build_cone_4x4"</td>
    </tr>
    <tr>
        <th>cone_effect_sell</th>
        <td>Defines the size / height of the selling drone when the building is being sold</td><td>string:"sell_big", string:"sell_medium", string:"sell_small"</td>
    </tr>
</table>  

## SkeletonDesc
The SkeletonDesc tells an entity to use a specific skeleton file. In this file, the bone location and connection are stored.  
```qml
SkeletonDesc
{
	name    "meshes/props/special/alien_structures/Modding_Tutorial"
}
```  

## LocalAabbDesc
Entity bounds ( LocalAabb ) is by default taken from the mesh, when the mesh is irregular/ has extending parts or is too small, you can override its bounds with LocalAabbDesc reducing or expanding the space it logically occupies.  
```qml
LocalAabbDesc
{
    local_aabb
    {
        min
        {
            x   "-2"
            y   "0"
            z   "-2"
        }
        max
        {
            x   "2"
            y   "0.1"
            z   "2"
        }	
    }
}
```  

# Animation
## AnimationDesc  
To make the entity play an animation on repeat (like a building doing something) add the following lines into the entity file.  
The `animName` depends on what the animation is called in Blender. You can also see the name in the model editor, being on the skeleton tab of the entity.  
![](../../../../assets/images/edit-entity-files-to-use-cutom-meshes.png)  
No idea what `animTime` does yet, 0.0 however, makes it play the whole animation just fine.  
```qml
AnimationDesc
{
    animations
    {
        Anim
        {
            animName    "hammering"
            animTime    "0.0"
        }
    }
}
```  
## AnimationGraphDesc
TBD  
```qml
AnimationGraphDesc
{
    animation_graph_name    "building_working"
}
```
  
# Common errors
- The mesh file flips around the player character and crashes on placement ->   
The entity uses a wrong skeleton file  
- The player character can walk through the object / other buildings can be placed into the mesh ->  
Wrong or missing physics