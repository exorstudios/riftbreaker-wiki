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
|:----------|:--------------|
| Vector< [Pair_uchar_TeamRelation](/riftbreaker-wiki/docs/game-reflection/classes/pair_uchar__team_relation/) > | relation_map |
| Vector< [TeamId](/riftbreaker-wiki/docs/game-reflection/classes/team_id/) > | parent_team_id_vec |
| Vector< [Pair_StringHash_TeamId](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_hash__team_id/) > | hash_to_team_id_map |
| Vector< [Pair_TeamId_String](/riftbreaker-wiki/docs/game-reflection/classes/pair__team_id__string/) > | team_id_to_name_map |
| Vector< [TeamId](/riftbreaker-wiki/docs/game-reflection/classes/team_id/) > | natural_order |
| Vector< [Pair_StringHash_uchar](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_hash_uchar/) > | relation_hash_to_map |
| Vector< [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) > | available_team_id_vec |
| Vector< [TeamMask](/riftbreaker-wiki/docs/game-reflection/enums/team_mask/) > | hierarchical_team_mask_vec |
| Vector< [Pair_TeamId_Vector_TeamId](/riftbreaker-wiki/docs/game-reflection/classes/pair__team_id__vector__team_id/) > | parent_to_children |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | relation_counter |

