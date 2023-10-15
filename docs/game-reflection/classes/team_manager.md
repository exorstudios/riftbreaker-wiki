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
| Vector< [Pair_uchar_TeamRelation](/docs/game-reflection/classes/pair_uchar__team_relation) > | relation_map |
| Vector< [TeamId](/docs/game-reflection/classes/team_id) > | parent_team_id_vec |
| Vector< [Pair_StringHash_TeamId](/docs/game-reflection/classes/pair__string_hash__team_id) > | hash_to_team_id_map |
| Vector< [Pair_TeamId_String](/docs/game-reflection/classes/pair__team_id__string) > | team_id_to_name_map |
| Vector< [TeamId](/docs/game-reflection/classes/team_id) > | natural_order |
| Vector< [Pair_StringHash_uchar](/docs/game-reflection/classes/pair__string_hash_uchar) > | relation_hash_to_map |
| Vector< [uint](/docs/game-reflection/components/uint) > | available_team_id_vec |
| Vector< [TeamMask](/docs/game-reflection/enums/team_mask) > | hierarchical_team_mask_vec |
| Vector< [Pair_TeamId_Vector_TeamId](/docs/game-reflection/classes/pair__team_id__vector__team_id) > | parent_to_children |
| [uint](/docs/game-reflection/components/uint) | relation_counter |

