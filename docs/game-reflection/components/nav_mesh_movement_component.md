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
|:-------------|:--------------|
| [bool](/docs/game-reflection/components/bool) | is_target_nearby |
| [uint](/docs/game-reflection/components/uint) | target_entity_id |
| [bool](/docs/game-reflection/components/bool) | should_calculate_path |
| [ushort](/docs/game-reflection/enums/ushort) | update_path_slot |
| [Vector3](/docs/game-reflection/classes/vector3) | velocity |
| [float](/docs/game-reflection/components/float) | angle_turn_speed |
| [uchar](/docs/game-reflection/enums/uchar) | state |
| [bool](/docs/game-reflection/components/bool) | is_only_separation |
| [float](/docs/game-reflection/components/float) | unit_soft_radius |
| [uint](/docs/game-reflection/components/uint) | ignore_cost_mask |
| [Vector3](/docs/game-reflection/classes/vector3) | target_origin |
| [uint](/docs/game-reflection/components/uint) | current_path_point_idx |
| [NullOnCopyPointer_CachedMovement](/docs/game-reflection/components/null_on_copy_pointer__cached_movement) | cached_movement |
| [bool](/docs/game-reflection/components/bool) | was_blocked |
| [bool](/docs/game-reflection/components/bool) | can_move |
| [int](/docs/game-reflection/enums/int) | current_node_index |
| [float](/docs/game-reflection/components/float) | acceleration |
| [uchar](/docs/game-reflection/enums/uchar) | type |
| Vector< [NavMeshMovementPoint](/docs/game-reflection/classes/nav_mesh_movement_point) > | path_points |
| [float](/docs/game-reflection/components/float) | max_speed |
| [Timer](/docs/game-reflection/classes/timer) | path_update_timer |
| [Vector3](/docs/game-reflection/classes/vector3) | seek_path_origin |
| Vector< [int](/docs/game-reflection/enums/int) > | flow_fields_indexes |
| [bool](/docs/game-reflection/components/bool) | always_in_motion |
| [float](/docs/game-reflection/components/float) | current_speed |
| [bool](/docs/game-reflection/components/bool) | is_target_visible |
| [Vector3](/docs/game-reflection/classes/vector3) | flow_fields_force |
| [ushort](/docs/game-reflection/enums/ushort) | dominance_group |
| [Vector3](/docs/game-reflection/classes/vector3) | force |

