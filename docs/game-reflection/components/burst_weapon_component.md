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
| [uint](/docs/game-reflection/components/uint) | muzzles_current_cycle |
| Vector< [Pair_uint_float](/docs/game-reflection/classes/pair_uint_float) > | reocils_tasks |
| Vector< [BurstFireRequest](/docs/game-reflection/classes/burst_fire_request) > | fire_requests |
| [bool](/docs/game-reflection/components/bool) | last_can_fire |
| [uchar](/docs/game-reflection/enums/uchar) | ammo_type |
| [float](/docs/game-reflection/components/float) | affector_time |
| [Entity](/docs/game-reflection/classes/entity) | last_snaped_ent |
| [bool](/docs/game-reflection/components/bool) | use_custom_target |
| Vector< [Entity](/docs/game-reflection/classes/entity) > | fire_loop_entities |
| Vector< [WeaponMuzzle](/docs/game-reflection/classes/weapon_muzzle) > | WeaponMuzzles |
| [uchar](/docs/game-reflection/enums/uchar) | current_state |
| [bool](/docs/game-reflection/components/bool) | plain_auto_aim |
| [float](/docs/game-reflection/components/float) | burst_column_angle |
| [bool](/docs/game-reflection/components/bool) | check_target_visibility |
| [Vector3](/docs/game-reflection/classes/vector3) | custom_target |
| [float](/docs/game-reflection/components/float) | burst_column_spacing |
| [WeaponAffector](/docs/game-reflection/classes/weapon_affector) | WeaponAffector |
| [IdString](/docs/game-reflection/components/id_string) | muzzle_flash_effect |
| [float](/docs/game-reflection/components/float) | burst_rate |
| [uint](/docs/game-reflection/components/uint) | muzzles_per_fire |
| [IdString](/docs/game-reflection/components/id_string) | fire_effect |
| [uchar](/docs/game-reflection/enums/uchar) | pending_state |
| [LogicTimer](/docs/game-reflection/classes/logic_timer) | reload_timer |
| [IdString](/docs/game-reflection/components/id_string) | ammo_blueprint |

