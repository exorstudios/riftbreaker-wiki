---
layout: default
title: MeshComponent
has_children: false
parent: Component
grand_parent: Game Reflection
---
# MeshComponent( [ RenderableComponent ](/riftbreaker-wiki/docs/game-reflection/components/renderable_component/) )
Description 

## Fields

| Type | Name |
|:----------|:--------------|
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | mesh |
| [IdString](/riftbreaker-wiki/docs/game-reflection/components/id_string/) | material |
| Container< [Pair_SubMeshSlotKey_int](/riftbreaker-wiki/docs/game-reflection/classes/pair__sub_mesh_slot_key_int/) > | subMeshSlotToIdx |
| Container< [Pair_uint64_SmallVector_1IdString](/riftbreaker-wiki/docs/game-reflection/classes/pair_uint64__small_vector_1_id_string/) > | materialIdMap |
| Container< [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) > | render_group |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | is_dirty |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | teleport_on_next_synchronize |

