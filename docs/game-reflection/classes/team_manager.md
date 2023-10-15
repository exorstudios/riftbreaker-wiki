---
layout: default
title: TeamManager
has_children: false
parent: Class
grand_parent: Game Reflection
---
# TeamManager
Description 

## Fields
| Type | Name |
|:-------------|:--------------|
| Vector< [Pair_uchar_TeamRelation](/game-reflection/classes/pair_uchar__team_relation.md) > | relation_map |
| Vector< [TeamId](/game-reflection/classes/team_id.md) > | parent_team_id_vec |
| Vector< [Pair_StringHash_TeamId](/game-reflection/classes/pair__string_hash__team_id.md) > | hash_to_team_id_map |
| Vector< [Pair_TeamId_String](/game-reflection/classes/pair__team_id__string.md) > | team_id_to_name_map |
| Vector< [TeamId](/game-reflection/classes/team_id.md) > | natural_order |
| Vector< [Pair_StringHash_uchar](/game-reflection/classes/pair__string_hash_uchar.md) > | relation_hash_to_map |
| Vector< [uint](/game-reflection/components/uint.md) > | available_team_id_vec |
| Vector< [TeamMask](/game-reflection/enums/team_mask.md) > | hierarchical_team_mask_vec |
| Vector< [Pair_TeamId_Vector_TeamId](/game-reflection/classes/pair__team_id__vector__team_id.md) > | parent_to_children |
| [uint](/game-reflection/components/uint.md) | relation_counter |
