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
|:----------|:--------------|
| [WeaponAffector](/riftbreaker-wiki/docs/game-reflection/classes/weapon_affector/) | WeaponAffector |
| [LogicTimer](/riftbreaker-wiki/docs/game-reflection/classes/logic_timer/) | reload_timer |
| Container< [BurstFireRequest](/riftbreaker-wiki/docs/game-reflection/classes/burst_fire_request/) > | fire_requests |
| Container< [WeaponMuzzle](/riftbreaker-wiki/docs/game-reflection/classes/weapon_muzzle/) > | WeaponMuzzles |
| Container< [Pair_uint_float](/riftbreaker-wiki/docs/game-reflection/classes/pair_uint_float/) > | reocils_tasks |
| Container< [Entity](/riftbreaker-wiki/docs/game-reflection/classes/entity/) > | fire_loop_entities |
| [Entity](/riftbreaker-wiki/docs/game-reflection/classes/entity/) | last_snaped_ent |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | custom_target |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | fire_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | muzzle_flash_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | ammo_blueprint |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | affector_time |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | burst_rate |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | burst_column_angle |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | burst_column_spacing |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | muzzles_per_fire |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | muzzles_current_cycle |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | check_target_visibility |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | plain_auto_aim |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | last_can_fire |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | use_custom_target |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | ammo_type |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | current_state |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | pending_state |

