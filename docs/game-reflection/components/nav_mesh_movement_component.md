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
|:------------ - | : -------------- |
| [bool](game-reflection/components/bool.md) | is_target_nearby |
| [uint](game-reflection/components/uint.md) | target_entity_id |
| [bool](game-reflection/components/bool.md) | should_calculate_path |
| [ushort](game-reflection/enums/ushort.md) | update_path_slot |
| [Vector3](game-reflection/classes/vector3.md) | velocity |
| [float](game-reflection/components/float.md) | angle_turn_speed |
| [uchar](game-reflection/enums/uchar.md) | state |
| [bool](game-reflection/components/bool.md) | is_only_separation |
| [float](game-reflection/components/float.md) | unit_soft_radius |
| [uint](game-reflection/components/uint.md) | ignore_cost_mask |
| [Vector3](game-reflection/classes/vector3.md) | target_origin |
| [uint](game-reflection/components/uint.md) | current_path_point_idx |
| [NullOnCopyPointer_CachedMovement](game-reflection/components/null_on_copy_pointer__cached_movement.md) | cached_movement |
| [bool](game-reflection/components/bool.md) | was_blocked |
| [bool](game-reflection/components/bool.md) | can_move |
| [int](game-reflection/enums/int.md) | current_node_index |
| [float](game-reflection/components/float.md) | acceleration |
| [uchar](game-reflection/enums/uchar.md) | type |
| Vector< [NavMeshMovementPoint](game-reflection/classes/nav_mesh_movement_point.md) > | path_points |
| [float](game-reflection/components/float.md) | max_speed |
| [Timer](game-reflection/classes/timer.md) | path_update_timer |
| [Vector3](game-reflection/classes/vector3.md) | seek_path_origin |
| Vector< [int](game-reflection/enums/int.md) > | flow_fields_indexes |
| [bool](game-reflection/components/bool.md) | always_in_motion |
| [float](game-reflection/components/float.md) | current_speed |
| [bool](game-reflection/components/bool.md) | is_target_visible |
| [Vector3](game-reflection/classes/vector3.md) | flow_fields_force |
| [ushort](game-reflection/enums/ushort.md) | dominance_group |
| [Vector3](game-reflection/classes/vector3.md) | force |
