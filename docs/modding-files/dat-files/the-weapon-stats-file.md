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
Sets a single value with optional min/max value for randomization. Just used for weapons and item typically.

### max_value
Sets a max value, used by `BASE_MINMAX` and optionally `BASE_DEFAULT`.

### min_value
Sets a min value, used by `BASE_MINMAX` and optionally `BASE_DEFAULT`.

### stat_features
Special stats which describe the general value behaviour of an entity.  
Available stat features:  

{: .highlight }
base_default or base_minmax is mandatory for everything, other fields are optional

| Stat feature | Purpose |
|:-------------|:-------------|
| BASE_DEFAULT | Default single value with added optional value range for randomization used in higher tier items |
| BASE_MINMAX | Random value range, it is randomized everytime a weapon is created |
| MODABLE | Allows modding with weapon mods in gui |
| HIDDEN | Hides this value from inventory menu, used for statistics that are always the same or others that EXOR does not want to show but are necessary for gameplay |
| STATISTIC | Makes this value "important" highlighted in inventory menu or makes it appear in small brackets, up to three values per item can be highlighted as important |
| INITIAL_RANDOMIZABLE | Used in higher tier items, adds this statistic to a random pool that is initialy boosted when crating an item, one statistic is boosted in advanced items, three are boosted in extreme items |

### stat_type
A special stat which describes the stat type of an entity.  
Available stat types:  

| Stat feature | Unit of measurement | Purpose |
|:-------------|:-------------|:-------------|
| AMMO_ANGLE_SPEED | degrees per second | This is projectile property, used only in weapons with ammo_homing, sets how fast projectiles can turn, high speed projectiles need much higher values to be effective |
| AMMO_AUTOAIM | degrees | This is weapon property, width of an autoaiming cone, weapons shoot projectiles "off the aiming line" straight at the closest target included in this aiming cone |
| AMMO_CLUSTER | percent | Number of new projectiles spawned at collision with world or an enemy, default 0, 1.5 means 100% chance for one cluster projectile at collision and 50% for another one |
| AMMO_COST | ammo | Ammo used per single projectile or per second in continuous weapons like laser or flamer |
| AMMO_HOMING | bool | This is projectile property, just a switch "on/off" - 0 means homing projectiles are disabled, 100 means homing projectiles are enabled, must be used with `ammo_angle_speed` |
| AMMO_SPEED | meters per second | Projectile speed |
| AMMO_SPREAD | degrees | Adds random aiming deviation to projectiles fired |
| AMMO_STUN | percent | Chance for stunning an enemy with every hit, enemies may have stun cooldowns or stun resistance |
| AMMO_STUN_LENGTH | seconds | Duration of stun |
| BEAM_RANGE | meter | Range of the beam or a flamer fire stream |
| BEAM_WIDTH | meter | Width of the beam or a flamer fire stream |
| DAMAGE_CRITICAL_CHANCE | percent | Chance for higher damage, calculated with every shot that hits an enemy, 5 means 5% chance for damage multiplied by `damage_critical_factor` percentage |
| DAMAGE_CRITICAL_FACTOR | percent | Critical multiplier for basic damage value, 500 means five times more damage than usual |
| DAMAGE_LIFESTEAL | hitpoints recovered per hit | Weapons with lifesteal recover a set number of hitpoints per every succeful hit, 1 means one hitpoint recovered per hit |
| DAMAGE_OVER_TIME | damage per second | Value of damage dealt per one second when damage over time effect is active |
| DAMAGE_OVER_TIME_LENGTH | seconds | Length of damage over time effect |
| DAMAGE_PENETRATION | percent | Number of targets that can be pierced by a projectile, default 0, 1.5 means 100% chance to pierce one enemy and 50% to pierce another one |
| DAMAGE_SPLASH | meter | Radius where damage is still applied |
| DAMAGE_SPREAD | percent | Damage random deviation, 5 means that there is up to 5% random damage addition or reduction (95%-105%) |
| DAMAGE_VALUE | damage points | Damage done by a single projectile or per second in continuous weapons like laser or flamer |
| FIRE_PER_BURST | projectiles per burst | Number of projectiles fire in short succession, 1.5 means that there is 50% chance for an addidtional projectile |
| FIRE_PER_SHOT | projectiles per shot | Number of projectiles fired simultaneously, 1.5 means that there is 50% chance for an addidtional projectile |
| FIRE_RATE | projectiles per second | Number of projectiles fired per second |
| WEAPON_SCALE | percent | Scale of projectiles, muzzle effects and hit effects, <br/>1 is 100% |
| WEAPON_ANIMATION_SPEED | percent | Does not work? Should change animation speed, <br/>1 is 100% |