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
## Multiplayer change game mode name
To change the game mode name which appears at the top of the multiplayer settings page,  
edit the file `\gui\00_multiplayer_dm_localizations.csv`

## Multiplayer change game mode picture
To change the game mode picture which appears at the top of the multiplayer settings page,  
edit the file `\campaigns\mp_deathmatch.campaign`  
There is a line called `preview_material` which points to a material file.  
That file can be found in `\materials\scripts\gui_menu_previews.material`.  
Now copy an existing preview and rename it to your mod, like:  
```qml
material gui/menu/campaign_prev/gungame_prev : gui/default
{
	set_texture_alias diffuse materials/textures/gui/menu/biomes_prev/gungame_prev.dds
}
```
Place the new game mode picture in the folder `\materials\textures\gui\menu\biomes_prev`, use the same filename as in the material file.  

{: .highlight }
A picture dimension of 710x150 is recommended.


## Multiplayer slider settings
Open file `\campaigns\mp_deathmatch.campaign` and edit `CampaignCustomOption` for slider handling  
In Lua the setting can be used as:  
```lua
local campaignData = CampaignService:GetCampaignData()
g_max_level = campaignData:GetIntOrDefault("max_level", 5)
```
Where `max_level` equals the `CampaignCustomOption` name.