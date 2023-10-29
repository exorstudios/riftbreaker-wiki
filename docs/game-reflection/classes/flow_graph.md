---
layout: default
title: FlowGraph
has_children: false
parent: Class
grand_parent: Game Reflection
---
# FlowGraph
Description 

## Fields

| Type | Name |
|:----------|:--------------|
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | template_name |
| [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) | template_version |
| Container< [Node](/riftbreaker-wiki/docs/game-reflection/classes/node/) > | nodes |
| Container< [Pair_StringHash_uint64](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_hash_uint64/) > | name_to_node |
| Container< [Edge](/riftbreaker-wiki/docs/game-reflection/classes/edge/) > | edges |
| Container< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | start_indices |
| Container< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | end_indices |
| Container< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | active_indices |
| Container< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | pending_indices |
| Container< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | disabled_indices |
| [FlowGraphCustomizer1](/riftbreaker-wiki/docs/game-reflection/components/flow_graph_customizer1/) | customizer |
| [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) | status |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | update_disabled_nodes |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | initialized |

