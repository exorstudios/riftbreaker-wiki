---
layout: default
title: PhysicsObjectDesc
has_children: false
parent: Component
grand_parent: Game Reflection
---
# PhysicsObjectDesc
Description 

## Fields

| Type | Name |
|:----------|:--------------|
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | group_id |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | create_flags |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | physics_material |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | physics_user_flag_mask |
| Container< [PhysicsShape](/riftbreaker-wiki/docs/game-reflection/classes/physics_shape/) > | Shapes |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | initial_force |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | linear_velocity |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | angular_velocity |
| [Vector3](/riftbreaker-wiki/docs/game-reflection/classes/vector3/) | inertia |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | associated_bone |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | density |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | mass |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | contact_offset |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | rest_offset |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | min_velocity_iteration_count |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | min_position_iteration_count |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | sleep_threshold |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | dominance |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | linear_damping |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | angular_damping |

