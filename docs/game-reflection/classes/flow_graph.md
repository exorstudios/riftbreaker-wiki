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
| [uint64](/game-reflection/components/uint64.md) | template_version |
| Vector< [uint64](/game-reflection/components/uint64.md) > | active_indices |
| [bool](/game-reflection/components/bool.md) | initialized |
| Vector< [uint64](/game-reflection/components/uint64.md) > | pending_indices |
| [bool](/game-reflection/components/bool.md) | update_disabled_nodes |
| Vector< [Pair_StringHash_uint64](/game-reflection/classes/pair__string_hash_uint64.md) > | name_to_node |
| [String](/game-reflection/components/string.md) | template_name |
| Vector< [uint64](/game-reflection/components/uint64.md) > | start_indices |
| Vector< [uint64](/game-reflection/components/uint64.md) > | end_indices |
| Vector< [Edge](/game-reflection/classes/edge.md) > | edges |
| Vector< [Node](/game-reflection/classes/node.md) > | nodes |
| [FlowGraphCustomizer1](/game-reflection/components/flow_graph_customizer1.md) | customizer |
| [int](/game-reflection/enums/int.md) | status |
| Vector< [uint64](/game-reflection/components/uint64.md) > | disabled_indices |
