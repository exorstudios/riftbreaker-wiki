---
layout: default
title: Multiplayer quick information
parent: Misc
nav_order: 1
---

# Information

This page serves as a quick and dirty information cheat-sheet for multiplayer modding

# Lua
## Player
```lua
PlayerService:GetPlayersMechs()
PlayerService:GetAllPlayers()
PlayerService:GetPlayerByMech( entity )
PlayerService:GetPlayerControlledEnt( player_id )
PlayerService:ResetDeathStats()
```

## Team
```lua
local team = EntityService:GetTeam( "player" )
EntityService:SetTeamRelation( team, team, "hostility" )
local player_team = PlayerService:CreatePlayerTeam("player_" .. tostring(player_id), true)
PlayerService:GetPlayerTeam(player_id)
PlayerService:SetPlayerTeam( player_id, player_team )
```

## Bots
```lua
local player_id = PlayerService:CreateFakePlayer();
local player_team = PlayerService:CreatePlayerTeam("bot_" .. tostring(player_id), true)
PlayerService:RemovePlayerBot(player_id)
PlayerService:CreatePlayerBot("player/character_bot", player_id, player_team )
```

## Misc
```lua
PlayerService:GetPlayerSpawnPoint( player_id )
ConsoleService:GetConfig("server_max_players_count")
CampaignService:ChangeCurrentMission( newMissionName )
```

# GUI
## Multiplayer slider settings
Open file `\campaigns\mp_deathmatch.campaign` and edit `CampaignCustomOption` for slider handling  
In Lua the setting can be used as:  
```lua
local campaignData = CampaignService:GetCampaignData()
g_max_level = campaignData:GetIntOrDefault("max_level", 5)
```
Where `max_level` equals the `CampaignCustomOption` name.

## Multiplayer change game mode name
To change the game mode name which appears at the top of the multiplayer settings page,  
edit the file `\gui\00_multiplayer_dm_localizations.csv`