---
layout: default
title: State class
parent: Misc
nav_order: 3
---

# Information

When working with states, the state class is used to access and modify state information.  
It can't be used any other way.  


# Functions
  
```qml
state:GetDurationLimit()
state:GetDuration()
state:SetDurationLimit( time )
state:SetUpdateInterval( interval )
state:Exit()
```

## Example

```qml
function drill:OnDrillStartEnter( state )
	state:SetDurationLimit( 0.75 )
end
```