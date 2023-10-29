---
layout: default
title: MissionDef
has_children: false
parent: Class
grand_parent: Game Reflection
---
# MissionDef
Description 

## Fields

| Type | Name |
|:----------|:--------------|
| [TileCoord](/riftbreaker-wiki/docs/game-reflection/classes/tile_coord/) | map_size |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | script |
| [Database](/riftbreaker-wiki/docs/game-reflection/components/database/) | script_database |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | localization_id |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | logic |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | biomes |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | description |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | preview_material |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | player_spawn_logic |
| [String](/riftbreaker-wiki/docs/game-reflection/components/string/) | mission_award |
| Container< [Pair_StringTileSpawnRule](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_tile_spawn_rule/) > | tile_spawn_rules |
| Container< [String](/riftbreaker-wiki/docs/game-reflection/components/string/) > | source_tiles |
| [uint64](/riftbreaker-wiki/docs/game-reflection/components/uint64/) | map_generator_seed |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | gravity_scale |
| Container< [ResourceVolume](/riftbreaker-wiki/docs/game-reflection/classes/resource_volume/) > | random_resources |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | max_starting_distance |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | min_starting_distance |
| Container< [ResourceVolume](/riftbreaker-wiki/docs/game-reflection/classes/resource_volume/) > | starting_resources |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | block_outpost_remove |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | detector_disabled |
| [bool](/riftbreaker-wiki/docs/game-reflection/components/bool/) | find_not_reachable_navigation |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | threat |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | creature_volumes_respawn_time_factor |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | creature_volumes_min_distance |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | creature_volumes_density |
| [float](/riftbreaker-wiki/docs/game-reflection/components/float/) | map_no_spawn_margin |
| Container< [Pair_String_VariantsVector](/riftbreaker-wiki/docs/game-reflection/classes/pair__string__variants_vector/) > | prefab_force_variants |
| Container< [Pair_String_VariantsVector](/riftbreaker-wiki/docs/game-reflection/classes/pair__string__variants_vector/) > | prefab_exclude_variants |
| Container< [Pair_String_Vector_CreatureVolume](/riftbreaker-wiki/docs/game-reflection/classes/pair__string__vector__creature_volume/) > | creature_volumes_species |
| Container< [Pair_String_AmbientCreatureVolume](/riftbreaker-wiki/docs/game-reflection/classes/pair__string__ambient_creature_volume/) > | ambient_creature_species |
| Container< [ObjectSpawner](/riftbreaker-wiki/docs/game-reflection/classes/object_spawner/) > | mission_object_spawners |
| [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) | failed_action |
| [int](/riftbreaker-wiki/docs/game-reflection/enums/int/) | success_action |
| Container< [Pair_StringTileSpawnRule](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_tile_spawn_rule/) > | light_mask_materials |
| Container< [Pair_StringTileSpawnRule](/riftbreaker-wiki/docs/game-reflection/classes/pair__string_tile_spawn_rule/) > | destructible_volume_texture_patterns |

