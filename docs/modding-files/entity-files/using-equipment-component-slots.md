---
layout: default
title: Using Equipment Component slots 
nav_order: 1
parent: Entity files
grand_parent: Modding files
---

# Information

In the Riftbreaker, towers can be modded just as the weapons of the mech.  
These mods are called weapon mods and enhance the tower in many different ways.  
Using the entity file, it is possible to allow other buildings to use mods too.
  
# EquipmentComponent
  
A great example of a building that allows for "slots" to be filled with an entity is the [Flora Cultivator](https://riftbreaker.fandom.com/wiki/Flora_Cultivator)  
As it allows to choose from all kind of different saplings it can plant.  
In the entity file of the Flora Cultivator you can find the code for it:  
```qml
EquipmentComponent
{
    equipment
    {
        Equipment Equipment
        {
            slots
            {        
                EquipmentSlot
                {
                    name            "MOD_1"
                    allow_types     "saplings"
                    subslots_count  "1"
                }                            
            }
        }
    }
}
```
The name of the EquipmentSlot can be `MOD_1`, `MOD_2`, `MOD_3` for all the available mod slots.  
The `allow_types` references the type of an entity in a blueprint, here it is in the file  
`items/loot/saplings/biomas_sapling_item`:  
```qml
EntityBlueprint
{ 
	name "items/loot/saplings/biomas_sapling_item"

	InventoryItemDesc
	{
		type            "saplings"
		name            "resource_name/biomas_sapling"
		icon            "gui/hud/flora/biomass_sapling_icon"
		bigger_icon     "gui/hud/flora/biomass_sapling_icon"
		is_persistant   "1"
	}

	DatabaseDesc
	{
		plant_prefab        string:"biomas_sapling"
		biome_requirement	string:"jungle"
	}
}
```  


{: .highlight }
Towers and weapons don't have the EquipmentComponent inside their entity file, since they have auto-generated EquipmentComponent based on level and receive mod slots based on quality.
