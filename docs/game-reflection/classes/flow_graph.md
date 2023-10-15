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
|:-------------|:--------------|
| [uint64](/docs/game-reflection/components/uint64) | template_version |
| Vector< [uint64](/docs/game-reflection/components/uint64) > | active_indices |
| [bool](/docs/game-reflection/components/bool) | initialized |
| Vector< [uint64](/docs/game-reflection/components/uint64) > | pending_indices |
| [bool](/docs/game-reflection/components/bool) | update_disabled_nodes |
| Vector< [Pair_StringHash_uint64](/docs/game-reflection/classes/pair__string_hash_uint64) > | name_to_node |
| [String](/docs/game-reflection/components/string) | template_name |
| Vector< [uint64](/docs/game-reflection/components/uint64) > | start_indices |
| Vector< [uint64](/docs/game-reflection/components/uint64) > | end_indices |
| Vector< [Edge](/docs/game-reflection/classes/edge) > | edges |
| Vector< [Node](/docs/game-reflection/classes/node) > | nodes |
| [FlowGraphCustomizer1](/docs/game-reflection/components/flow_graph_customizer1) | customizer |
| [int](/docs/game-reflection/enums/int) | status |
| Vector< [uint64](/docs/game-reflection/components/uint64) > | disabled_indices |

