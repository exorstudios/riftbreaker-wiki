---
layout: default
title: Events, Requests and RegisterHandler 
nav_order: 95
parent: Lua files
grand_parent: Modding files
---

# Information
Most of the communication between systems and entities is done asynchronously via events. That's why events and requests were created.  

An overview of events and requests can be found in the game reflection of the workspace editor. 
{: .highlight}  

# Requests
It is used when a system should do some job on behalf of an entity.

## Example
```qml
QueueEvent( "DamageRequest", target, 200.0, "physical", 1, 0 )
```
In that case, you are requesting some system to deal damage to an entity on your behalf.

# Events
It is a notification that something happened with an entity. 

## Example
So after DamageSystem handled the DamageRequest sent earlier (see above) and dealt damage to that entity, it sends a notification in form of a DamageEvent.  
To use an event, the entity needs to be able to "listen" for events, for that purpose the RegisterHandler is used.

## Functions
For event functions, see [Event class](../../../misc/event-class).

# RegisterHandler
Allows entities to "listen" for events / requests happening in the same or other files all around. 

## Example 1
```qml
self:RegisterHandler( event_sink, "DamageRequest", ... )
self:RegisterHandler( event_sink, "DamageEvent", ... )
```
## Explanation 1
Your function here will be called for all damage requests / events sent for all entities, it uses the `event_sink`.

event_sink: Your function will be called on this kind of request / event sent to **any** entity
{: .highlight}  

---

## Example 2
```qml
self:RegisterHandler( self.entity, "DamageRequest", ... )
self:RegisterHandler( self.entity, "DamageEvent", ... )
```

## Explanation 2
Uses this function only when someone requests / notifies damage on **this** entity and ignore everything else, it uses `self.entity`.

---

## Example 3
```qml
self:RegisterHandler( spawned_entity, "DamageRequest", ... )
self:RegisterHandler( spawned_entity, "DamageEvent", ... )
```

## Explanation 3
Uses this function only when someone request / notifies damage on entity `spawned_entity` and ignore everything else. Can add any known entity.

# UnregisterHandler
Stops "listening" for events / requests happening to entities

## Example
```qml
self:UnregisterHandler( event_sink, "DamageRequest", ... )
self:UnregisterHandler( event_sink, "DamageEvent", ... )
```