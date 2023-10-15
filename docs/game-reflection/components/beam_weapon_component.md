---
layout: default
title: BeamWeaponComponent
has_children: false
parent: Component
grand_parent: Game Reflection
---
# BeamWeaponComponent
Description 

## Fields
| Type | Name |
|:------------ - | : -------------- |
| [bool](game-reflection/components/bool.md) | last_can_fire |
| [uchar](game-reflection/enums/uchar.md) | ammo_type |
| [float](game-reflection/components/float.md) | affector_power |
| [Entity](game-reflection/classes/entity.md) | last_snaped_ent |
| Vector< [WeaponMuzzle](game-reflection/classes/weapon_muzzle.md) > | WeaponMuzzles |
| [uchar](game-reflection/enums/uchar.md) | current_state |
| [bool](game-reflection/components/bool.md) | plain_auto_aim |
| [uint64](game-reflection/components/uint64.md) | autoaim_type |
| [bool](game-reflection/components/bool.md) | check_target_visibility |
| [float](game-reflection/components/float.md) | cooldown_time |
| [WeaponAffector](game-reflection/classes/weapon_affector.md) | WeaponAffector |
| [LogicTimer](game-reflection/classes/logic_timer.md) | cooldown_timer |
| Vector< [Pair_IdString_Vector_Entity](game-reflection/classes/pair__id_string__vector__entity.md) > | children_entities |
| [IdString](game-reflection/components/id_string.md) | fire_effect |
| [uchar](game-reflection/enums/uchar.md) | pending_state |
| [IdString](game-reflection/components/id_string.md) | ammo_blueprint |
