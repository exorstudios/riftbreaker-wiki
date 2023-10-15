---
layout: default
title: MeshComponent
has_children: false
parent: Component
grand_parent: Game Reflection
---
# MeshComponent( ![ RenderableComponent ](game-reflection/components/renderable_component.md) )
Description 

## Fields
| Type | Name |
|:------------ - | : -------------- |
| [IdString](game-reflection/components/id_string.md) | material |
| [uchar](game-reflection/enums/uchar.md) | teleport_on_next_synchronize |
| [IdString](game-reflection/components/id_string.md) | mesh |
| Vector< [uchar](game-reflection/enums/uchar.md) > | render_group |
| Vector< [Pair_uint64_SmallVector_1IdString](game-reflection/classes/pair_uint64__small_vector_1_id_string.md) > | materialIdMap |
| [bool](game-reflection/components/bool.md) | is_dirty |
| Vector< [Pair_SubMeshSlotKey_int](game-reflection/classes/pair__sub_mesh_slot_key_int.md) > | subMeshSlotToIdx |
