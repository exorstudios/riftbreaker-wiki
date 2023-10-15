---
layout: default
title: NavMeshMovementComponent
has_children: false
parent: Component
grand_parent: Game Reflection
---
# NavMeshMovementComponent
Description 

## Fields

| Type | Name |
|:----------|:--------------|
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_target_nearby |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | target_entity_id |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | should_calculate_path |
| [ushort](/riftbreaker-wiki/docs/game-reflection/enums/ushort/) | update_path_slot |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | velocity |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | angle_turn_speed |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | state |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_only_separation |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | unit_soft_radius |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | ignore_cost_mask |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | target_origin |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | current_path_point_idx |
| [NullOnCopyPointer_CachedMovement](/riftbreaker-wiki/docs/game-reflection/components/null_on_copy_pointer__cached_movement/) | cached_movement |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | was_blocked |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | can_move |
| [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) | current_node_index |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | acceleration |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | type |
| Vector< [NavMeshMovementPoint](/riftbreaker-wiki/docs/game-reflection/classes/nav_mesh_movement_point/) > | path_points |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | max_speed |
| [Timer](/riftbreaker-wiki/docs/game-reflection/classes/timer/) | path_update_timer |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | seek_path_origin |
| Vector< [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) > | flow_fields_indexes |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | always_in_motion |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | current_speed |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_target_visible |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | flow_fields_force |
| [ushort](/riftbreaker-wiki/docs/game-reflection/enums/ushort/) | dominance_group |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | force |

