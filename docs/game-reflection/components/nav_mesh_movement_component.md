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
| [NullOnCopyPointer_CachedMovement](/riftbreaker-wiki/docs/game-reflection/components/null_on_copy_pointer__cached_movement/) | cached_movement |
| Container< [NavMeshMovementPoint](/riftbreaker-wiki/docs/game-reflection/classes/nav_mesh_movement_point/) > | path_points |
| Container< [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) > | flow_fields_indexes |
| [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) | current_node_index |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | target_origin |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | target_entity_id |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | current_speed |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | max_speed |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | angle_turn_speed |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | acceleration |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | velocity |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | force |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | flow_fields_force |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | unit_soft_radius |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | ignore_cost_mask |
| [Timer](/riftbreaker-wiki/docs/game-reflection/classes/timer/) | path_update_timer |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | seek_path_origin |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | current_path_point_idx |
| [ushort](/riftbreaker-wiki/docs/game-reflection/enums/ushort/) | dominance_group |
| [ushort](/riftbreaker-wiki/docs/game-reflection/enums/ushort/) | update_path_slot |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | state |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | type |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | can_move |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_target_visible |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | should_calculate_path |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_target_nearby |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_only_separation |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | always_in_motion |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | was_blocked |

