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


