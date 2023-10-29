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
| Container< [TeamMask](/riftbreaker-wiki/docs/game-reflection/enums/team_mask/) > | hierarchical_team_mask_vec |
| Container< [TeamId](/riftbreaker-wiki/docs/game-reflection/classes/team_id/) > | natural_order |
| Container< [Pair_TeamId_Vector_TeamId](/riftbreaker-wiki/docs/game-reflection/classes/pair__team_id__vector__team_id/) > | parent_to_children |
| Container< [TeamId](/riftbreaker-wiki/docs/game-reflection/classes/team_id/) > | parent_team_id_vec |
| Container< [Pair_StringHash_TeamId](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_hash__team_id/) > | hash_to_team_id_map |
| Container< [Pair_TeamId_String](/riftbreaker-wiki/docs/game-reflection/classes/pair__team_id__string/) > | team_id_to_name_map |
| Container< [Pair_StringHash_uchar](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_hash_uchar/) > | relation_hash_to_map |
| Container< [Pair_uchar_TeamRelation](/riftbreaker-wiki/docs/game-reflection/classes/pair_uchar__team_relation/) > | relation_map |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | relation_counter |
| Container< [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) > | available_team_id_vec |

