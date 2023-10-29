---
layout: default
title: ResourceConverterComponent
has_children: false
parent: Component
grand_parent: Game Reflection
---
# ResourceConverterComponent
Description 

## Fields

| Type | Name |
|:----------|:--------------|
| [ResourceBasket](/riftbreaker-wiki/docs/game-reflection/classes/resource_basket/) | local_basket |
| Container< [GameplayResourceDefHolder](/riftbreaker-wiki/docs/game-reflection/components/gameplay_resource_def_holder/) > | all_resources |
| Container< [GameplayResourceDefHolder](/riftbreaker-wiki/docs/game-reflection/components/gameplay_resource_def_holder/) > | optional_resources |
| Container< [StringHash](/riftbreaker-wiki/docs/game-reflection/classes/string_hash/) > | missing_resources |
| Container< [Pair_StringHash_String](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_hash__string/) > | resources_family |
| Container< [Pair_GameplayResourceDefHolder_float](/riftbreaker-wiki/docs/game-reflection/classes/pair__gameplay_resource_def_holder_float/) > | resources_radius |
| Container< [Pair_GameplayResourceDefHolder_Vector_Entity](/riftbreaker-wiki/docs/game-reflection/classes/pair__gameplay_resource_def_holder__vector__entity/) > | vein |
| [uint](/riftbreaker-wiki/docs/game-reflection/components/uint/) | energy_graphs |
| [ModifiableValue](/riftbreaker-wiki/docs/game-reflection/classes/modifiable_value/) | effectiveness |
| [ModifiableValue](/riftbreaker-wiki/docs/game-reflection/classes/modifiable_value/) | cost_modifier |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | last_ore_produced |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | update_interval |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | reset_interval |
| [Timer](/riftbreaker-wiki/docs/game-reflection/classes/timer/) | reset_timer |
| [Timer](/riftbreaker-wiki/docs/game-reflection/classes/timer/) | update_timer |
| Container< [float](/riftbreaker-wiki/docs/game-reflection/components/float/) > | working_time |
| [Bitset16](/riftbreaker-wiki/docs/game-reflection/components/bitset16/) | in_mask |
| [Bitset16](/riftbreaker-wiki/docs/game-reflection/components/bitset16/) | out_mask |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | priority |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | status |
| [uchar](/riftbreaker-wiki/docs/game-reflection/enums/uchar/) | mode |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | one_vein_mode |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | initialized |
| Container< [Pair_String_Vector_StringHash](/riftbreaker-wiki/docs/game-reflection/classes/pair__string__vector__string_hash/) > | family_acomplish_map |

