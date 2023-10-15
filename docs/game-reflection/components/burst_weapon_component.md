---
layout: default
title: BurstWeaponComponent
has_children: false
parent: Component
grand_parent: Game Reflection
---
# BurstWeaponComponent
Description 

## Fields
| Type | Name |
|:-------------|:--------------|
| [uint](/game-reflection/components/uint.md) | muzzles_current_cycle |
| Vector< [Pair_uint_float](/game-reflection/classes/pair_uint_float.md) > | reocils_tasks |
| Vector< [BurstFireRequest](/game-reflection/classes/burst_fire_request.md) > | fire_requests |
| [bool](/game-reflection/components/bool.md) | last_can_fire |
| [uchar](/game-reflection/enums/uchar.md) | ammo_type |
| [float](/game-reflection/components/float.md) | affector_time |
| [Entity](/game-reflection/classes/entity.md) | last_snaped_ent |
| [bool](/game-reflection/components/bool.md) | use_custom_target |
| Vector< [Entity](/game-reflection/classes/entity.md) > | fire_loop_entities |
| Vector< [WeaponMuzzle](/game-reflection/classes/weapon_muzzle.md) > | WeaponMuzzles |
| [uchar](/game-reflection/enums/uchar.md) | current_state |
| [bool](/game-reflection/components/bool.md) | plain_auto_aim |
| [float](/game-reflection/components/float.md) | burst_column_angle |
| [bool](/game-reflection/components/bool.md) | check_target_visibility |
| [Vector3](/game-reflection/classes/vector3.md) | custom_target |
| [float](/game-reflection/components/float.md) | burst_column_spacing |
| [WeaponAffector](/game-reflection/classes/weapon_affector.md) | WeaponAffector |
| [IdString](/game-reflection/components/id_string.md) | muzzle_flash_effect |
| [float](/game-reflection/components/float.md) | burst_rate |
| [uint](/game-reflection/components/uint.md) | muzzles_per_fire |
| [IdString](/game-reflection/components/id_string.md) | fire_effect |
| [uchar](/game-reflection/enums/uchar.md) | pending_state |
| [LogicTimer](/game-reflection/classes/logic_timer.md) | reload_timer |
| [IdString](/game-reflection/components/id_string.md) | ammo_blueprint |
