---
layout: default
title: weapon_stats file
nav_order: 2
parent: Dat files
grand_parent: Modding files
---

# Information

The `weapon_stats.dat` file is used to assign damage values, damage types, damage features to anything doing damage. Like items, skills, weapons, towes, drones, units etc.  
This file is actually a replacement of the WeaponItemDesc which would normally required in every file for items, skills, weapons, towes, drones, units etc.  
So instead of tuning vales in every single file, this file has it all combined and can also be edited in the Riftbreaker Editor.  
  
# Parameters explained
## ammo_storage
Is only used for player weapons and towers and sets which kind of ammo they consume by firing.  
Available storages:  

| Player weapons | Towers |
|:-------------|:-------------|
| ammo_mech_energy_cell, ammo_mech_explosive, ammo_mech_low_caliber, ammo_mech_high_caliber, ammo_mech_liquid | energy, ammo_tower_liquid, ammo_tower_explosive, ammo_tower_low_caliber |

If a tower or weapon isn't using any ammo storage, it might not consume ammo (melee weapons f.e) or it got balanced in another way, f.e having an upkeep of a rare liquid instead of energy (like the morphium tower).

---

## damage_type
Damage types set the kind of damage a projectile/weapon/enemy is doing.  
Available damage types:  

| Damage types |
|:-------------|
| physical, acid, area, fire, cryo, energy |

---

## rarity
Rarities set the quality of an entity. It's typically seperated in 4 rarities (worst/lowest to best/highest): Standard, Advanced, Superior, Extreme.  
Weapons can be crafted as Standard quality. Towers, however, start as level 1 with Advanced quality.

| Rarity levels weapons | Rarity levels towers |
|:-------------|:-------------|
| Standard, Advanced, Superior, Extreme | Advanced, Superior, Extreme |

Rarities for weapons and towers set their available weapon mod slots:  

| Standard | Advanced | Superior | Extreme |
|:-------------|:-------------|:-------------|:-------------|
| 0 mod slots | 1 mod slot | 2 mod slots | 3 mod slots |

---

## WeaponStatDef
This part is seperated into even more parameters which describe the actual damage as well as special stats.

### default_value
Is only available when the stats_feature `BASE_DEFAULT` is given.  
Sets a default value which XXXXXXXX. Just used for weapons and item typically.

### max_value
Sets a max value.

### min_value
Sets a min value.

### stat_features
Special stats which describe the general value behaviour of an entity.  
Available stat features:  

| Stat feature | Purpose |
|:-------------|:-------------|
| BASE_DEFAULT | XXXXX |
| BASE_MINMAX | Damage distribution depends on min_value and max_value |
| MODABLE | Allows this stat to be modded using weapon mods |
| HIDDEN | XXXXX |
| STATISTIC | XXXXX |
| INITIAL_RANDOMIZABLE | XXXXX |

### stat_type
A special stat which describes the stat type of an entity.  
Available stat types:  

| Stat feature | Unit | Purpose |
|:-------------|:-------------|:-------------|
| AMMO_ANGLE_SPEED | | XXXXX |
| AMMO_AUTOAIM | | XXXXX |
| AMMO_CLUSTER | | XXXXX |
| AMMO_COST | | XXXXX |
| AMMO_HOMING | | XXXXX |
| AMMO_SPEED | | XXXXX |
| AMMO_SPREAD | | XXXXX |
| AMMO_STUN | | XXXXX |
| AMMO_STUN_LENGTH | | XXXXX |
| BEAM_RANGE | | XXXXX |
| BEAM_WIDTH | | XXXXX |
| DAMAGE_CRITICAL_CHANCE | | XXXXX |
| DAMAGE_CRITICAL_FACTOR | | XXXXX |
| DAMAGE_LIFESTEAL | | XXXXX |
| DAMAGE_OVER_TIME | | XXXXX |
| DAMAGE_OVER_TIME_LENGTH | | XXXXX |
| DAMAGE_PENETRATION | | XXXXX |
| DAMAGE_SPLASH | | XXXXX |
| DAMAGE_SPREAD | | XXXXX |
| DAMAGE_VALUE | | XXXXX |
| FIRE_PER_BURST | | XXXXX |
| FIRE_PER_SHOT | | XXXXX |
| FIRE_RATE | | XXXXX |
| WEAPON_SCALE | | XXXXX |
| WEAPON_ANIMATION_SPEED | | XXXXX |