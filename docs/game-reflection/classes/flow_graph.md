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
| [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) | template_version |
| Vector< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | active_indices |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | initialized |
| Vector< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | pending_indices |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | update_disabled_nodes |
| Vector< [Pair_StringHash_uint64](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_hash_uint64/) > | name_to_node |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | template_name |
| Vector< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | start_indices |
| Vector< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | end_indices |
| Vector< [Edge](/riftbreaker-wiki/docs/game-reflection/classes/edge/) > | edges |
| Vector< [Node](/riftbreaker-wiki/docs/game-reflection/classes/node/) > | nodes |
| [FlowGraphCustomizer1](/riftbreaker-wiki/docs/game-reflection/components/flow_graph_customizer1/) | customizer |
| [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) | status |
| Vector< [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) > | disabled_indices |

