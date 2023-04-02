---
layout: default
title: StateMachine
nav_order: 96
parent: Lua files
grand_parent: Modding files
---

# Information
The StateMachine, as the name suggests, watches over the different states of an entity.  
Most parts of a Lua file are single processed LUA functions which are done once every time they are used. States however, are like an active process - like the inner part of a while-loop. 

# The Riftbreaker Lua state
There are no pre-defined lists of states for the Lua files. Everyone can create states as they wish.   
It is best practice, to give it a fitting name though.
The most used/created state for buildings, is the state "working" - mostly because it has a big meaning and could be used for almost any building as most building do something all the time, and thus be "working". 

# Structure
The StateMachine consists of different parts:

## The creation of the StateMachine
Usually at the top of the LUA file, the StateMachine itself gets created.
```qml
self.fsm = self:CreateStateMachine()
```
## The creation of the states
Right after the creation of the StateMachine itself, the different states get created.
```qml
self.fsm:AddState( "building", { enter="_OnBuildingEnter", execute="_OnBuildingExecute", exit="_OnBuildingExit", interval=0.5" } )
```
That line consists of different components:

| Part       | Explanation     | Required |
|:-------------|:--------------|:--------------:|
| `building` | Is the name of the state. Can be named however you wish. <br/>As said before, best practice is to name it fitting to the action that is happening. | Yes |
| `from="*"` | Old stuff from X-Morph not supported/used anymore. <br/>Don't use | No |
| `enter="_OnBuildingEnter"` | When the entity "enters" the defined state (here "building"), do the function "_OnBuildingEnter".<br/>Executed only once on state enter  | No |
| `execute="_OnBuildingExecute"` | When the entity "executes" the defined state (here "building"), do the function "_OnBuildingExecute".<br/>Executed every tick/interval until state change/ duroation limit reached  | Yes |
| `exit="_OnBuildingExit"` | When the entity "exits" the defined state (here "building"), do the function "_OnBuildingExit".<br/>Executed only once on state exit  | No |
| `interval=0.5` | Tells the game how often this state needs to be executed, here each 0.5 seconds.<br/>Mostly used when looping a function without a state parameter. | No |

The 3 main parts in the { } brackets reflect the normal lifecycle of a state(Enter, Execute, Exit).  
It enters the state, it does the state, it exits the state.   
How and when it shall do these steps of the lifecycle depends on you.  
You also don't need to use all 3 of them, you could just have:
```qml
self.fsm:AddState( "idle", { execute="OnIdle" } )
```

## State switching
To switch between the states inside the code, you have to tell the game to change the state of an entity by using the name of the state:
```qml
self.fsm:ChangeState( "building" )
```
Like this, the state "building" switches to the next one. 

## State function triggering
After a state switches, the function which is defined in the creation of the states get executed. In the LUA file it would look like this:
```qml
self.fsm = self:CreateStateMachine()
self.fsm:AddState( "building", { enter="_OnBuildingEnter", execute="_OnBuildingExecute", exit="_OnBuildingExit" } )
self.fsm:ChangeState( "building" )
...
...


entity_name:_OnBuildingEnter ( state )
...
...
```
Since the state of "building" gets changed after creation, it would trigger the part of `enter="_OnBuildingEnter"`. That part would start the function `entity_name:_OnBuildingEnter ( state )` 


## State as parameter

States as parameters are generally like every other parameter, but they can look like
```qml
entity_name:_OnBuildingEnter ( state )
or 
entity_name:_OnBuildingEnter ( state, dt )
```

## State functions

See page: [State class](../../../misc/state-class)

