---
layout: default
title: Community Lua code
parent: Misc
nav_order: 5
---

# Information

This page lists Lua code examples created by the community itself.  
From the community - for the community.

# Functions
<details markdown="block">
  <summary>
    SwapVector
  </summary>

```lua
Created by Piisfun
09.05.23
------------------
--Prepare vectors for use with FindService:FindEntitiesInBox
function SwapVector(vector_1, vector_2)
  local temp = 0
  --Check X
  if vector_2.x < vector_1.x then
    --swap values
    temp = vector_2.x
    vector_2.x = vector_1.x
    vector_1.x = temp
  end
  --Check Y
  if vector_2.y < vector_1.y then
    --swap values
    temp = vector_2.y
    vector_2.y = vector_1.y
    vector_1.y = temp
  end
  --Check Z
  if vector_2.z < vector_1.z then
    --swap values
    temp = vector_2.z
    vector_2.z = vector_1.z
    vector_1.z = temp
  end
  return {vector_1, vector_2}
end
```

</details>

<details markdown="block">
  <summary>
    Get terrain type
  </summary>

```lua
Created by ponomaryow.dmitry
11.11.23
------------------
require("lua/utils/reflection.lua")
require("lua/utils/table_utils.lua")
require("lua/utils/string_utils.lua")
require("lua/utils/building_utils.lua")
require("lua/utils/numeric_utils.lua")

function ShouldBuildDesertFloor( position )

    local terrainType = ""

    local overrideTerrains = {}

    local terrainCellEntityId = EnvironmentService:GetTerrainCell(position)

    if ( terrainCellEntityId ~= nil and terrainCellEntityId ~= INVALID_ID ) then
        
        local terrainTypeLayerComponent = EntityService:GetComponent( terrainCellEntityId, "TerrainTypeLayerComponent" )

        if ( terrainTypeLayerComponent ~= nil ) then

            local terrainTypeLayerComponentRef = reflection_helper(terrainTypeLayerComponent)

            if ( terrainTypeLayerComponentRef.terrain_type and terrainTypeLayerComponentRef.terrain_type.resource and terrainTypeLayerComponentRef.terrain_type.resource.name ) then

                terrainType = terrainTypeLayerComponentRef.terrain_type.resource.name
            end
        end
        
        local overrideTerrainComponent = EntityService:GetComponent( terrainCellEntityId, "OverrideTerrainComponent" )

        if ( overrideTerrainComponent ~= nil ) then

            local overrideTerrainComponentRef = reflection_helper(overrideTerrainComponent)

            if ( overrideTerrainComponentRef.terrain_overrides ) then

                for i=1,overrideTerrainComponentRef.terrain_overrides.count do

                    local terrainTypeHolder = overrideTerrainComponentRef.terrain_overrides[i]

                    if ( terrainTypeHolder and terrainTypeHolder.resource and terrainTypeHolder.resource.name ) then

                        if ( IndexOf( overrideTerrains, terrainTypeHolder.resource.name ) == nil ) then
                            Insert( overrideTerrains, terrainTypeHolder.resource.name )
                        end
                    end
                end
            end
        end
    end

    local isQuickSand = (terrainType == "quicksand")
    local hasDesertFloor = (IndexOf( overrideTerrains, "desert_floor" ) ~= nil)

    if ( isQuickSand and not hasDesertFloor ) then

        return true
    end

    return false
end
```

</details>
