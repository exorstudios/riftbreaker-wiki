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
|:-------------|:--------------|
| [bool](/docs/game-reflection/components/bool) | last_can_fire |
| [uchar](/docs/game-reflection/enums/uchar) | ammo_type |
| [float](/docs/game-reflection/components/float) | affector_power |
| [Entity](/docs/game-reflection/classes/entity) | last_snaped_ent |
| Vector< [WeaponMuzzle](/docs/game-reflection/classes/weapon_muzzle) > | WeaponMuzzles |
| [uchar](/docs/game-reflection/enums/uchar) | current_state |
| [bool](/docs/game-reflection/components/bool) | plain_auto_aim |
| [uint64](/docs/game-reflection/components/uint64) | autoaim_type |
| [bool](/docs/game-reflection/components/bool) | check_target_visibility |
| [float](/docs/game-reflection/components/float) | cooldown_time |
| [WeaponAffector](/docs/game-reflection/classes/weapon_affector) | WeaponAffector |
| [LogicTimer](/docs/game-reflection/classes/logic_timer) | cooldown_timer |
| Vector< [Pair_IdString_Vector_Entity](/docs/game-reflection/classes/pair__id_string__vector__entity) > | children_entities |
| [IdString](/docs/game-reflection/components/id_string) | fire_effect |
| [uchar](/docs/game-reflection/enums/uchar) | pending_state |
| [IdString](/docs/game-reflection/components/id_string) | ammo_blueprint |

