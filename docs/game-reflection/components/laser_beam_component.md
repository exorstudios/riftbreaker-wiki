---
layout: default
title: LaserBeamComponent
has_children: false
parent: Component
grand_parent: Game Reflection
---
# LaserBeamComponent
Description 

## Fields

| Type | Name |
|:----------|:--------------|
| [PriorityTypeMask](/riftbreaker-wiki/docs/game-reflection/classes/priority_type_mask/) | damage_factor_exclude |
| Container< [Entity](/riftbreaker-wiki/docs/game-reflection/classes/entity/) > | ring_entities |
| Container< [LaserHitRequest](/riftbreaker-wiki/docs/game-reflection/classes/laser_hit_request/) > | beam_hit_requests |
| Container< [LaserHitEffect](/riftbreaker-wiki/docs/game-reflection/classes/laser_hit_effect/) > | beam_hit_effects |
| [DamagePattern](/riftbreaker-wiki/docs/game-reflection/classes/damage_pattern/) | DamagePattern |
| [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) | non_blocking_type |
| [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) | colliding_type |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | collision_user_mask |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | on_enemy_hit_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | on_world_hit_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | on_resisted_hit_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | on_reflected_hit_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | on_water_hit_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | on_shield_hit_effect |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | ring_bp |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | owner |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | creator |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | last_target |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | current_target |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | max_hits |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | collision_3d |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | collision_block |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | timer |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | current_damage_factor |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | desired_damage_factor |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | range |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | diameter |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | damage_factor_max |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | damage_factor_increase |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | damage_factor_decrease |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | damage_max_beam_scale |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | damage_max_beam_glow |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | friendly_fire |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_visible_only |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | only_blocking_effect |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | skip_update |

