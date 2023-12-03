---
layout: default
title: The Predicate
nav_order: 4
parent: Lua files
grand_parent: Modding files
---

# Information

Predicates are expressions that evaluate to either true or false and are used to thin out a dataset.  
They come in combination with pre-filters and filter.  
A use-case is typically a [Lua service](../../../lua-services) which uses predicates to precisely choose a particular type of entity out of a bigger pool.  
F.e.: `FindService:FindEntitiesByPredicateInRadius, FindService:FindEntitiesByPredicateInBox` etc.  

# Pre-Filters
## Signature

A predicate signature is meant to scan all entities for the [components](../../../game-reflection/components) given - either 1 or more components.  
With multiple components, an entity needs to have **all** of them to be included.  
### Example
```qml
signature="HealthComponent,BuildingComponent"
```  

## Type

Type reflects the type of an entity from their entity file.  
For units it's typically the type from TypeDesc with values like `ground_unit`, `ground_unit_large`, etc.  
For buildings it's typically the type from BuildingDesc with values like `tower`, `wall`, etc.  
Multiple entries can be combined by using | as a character.
### Example
```qml
type = "building|defense"
```  
## Blueprint

Blueprint narrows the pool of entities down to the specific blueprint given.
### Example
```qml
blueprint = "buildings/defense/wall_gate_crystal_lvl_2"
```  

## Team

Using the Team pre-filter, only entities of a particular team get selected.  
### Example
```qml
team = "player"
```  

## Name

Using the Name pre-filter, only entities with a particular entity name get selected.  
The name origins from the IdDesc/IdComponent of an entity.
### Example
```qml
name = "_rift_station_"
```  

## Group

Using the Group pre-filter, only entities of a particular group get selected.  
The group origins from the IdDesc/IdComponent of an entity.
### Example
```qml
group = "spawn_cavern_spline"
```  

# Filter

The Filter allows to further accept or deny entities to be returned based on custom logic.  
On multi stage filter rules, returns are added to include/exclude entities from the results.  
A `return true` means, that you want to include this entity in the result.  
A `return false` means, that you want to exclude this entity from the result.
## Example
### Single stage
```qml
filter = function( entity )
    return HealthService:GetHealthInPct( entity ) < 0.5
end
```  
### Multi stage
```qml
        filter = function(entity)
            if self:IsTargetLocked(entity, LOCK_TYPE_REPAIR) then
               return false
            end

            if not HealthService:IsAlive(entity) then
                return false
            end

            local health = HealthService:GetHealthInPercentage( entity )
            if health >= 1.0 then
                return false
            end

            return true
        end
```  

# Full predicate examples, simple to complex
```qml
// Find all entities with type = wall
local predicate = {
    type = "wall"
}

// Find all entities with type = wall that also have BuildingComponent
local predicate = {
    type = "wall",
    signature = "BuildingComponent"
}

// Find all entities with type = wall that also have BuildingComponent and belong to team "player"
local predicate = {
    type = "wall",
    signature = "BuildingComponent",
    team = "player",
}

// Find all entities with type = wall that also have BuildingComponent and belong to team "player" and are instance of blueprint = "buildings/defense/wall_gate_crystal_lvl_2"
local predicate = {
    type = "wall",
    signature = "BuildingComponent",
    team = "player",
    blueprint = "buildings/defense/wall_gate_crystal_lvl_2"
}

// Find all entities with type = wall that also have BuildingComponent and belong to team "player" and has less than 50% of health
local predicate = {
    type = "wall",
    signature = "BuildingComponent",
    team = "player",
    filter = function( entity )
      return HealthService:GetHealthInPct( entity ) < 0.5
    end
}

// Find all entities with type = wall that are instance of blueprint = "buildings/defense/wall_gate_crystal_lvl_2"
local predicate = {
    team = "player",
    blueprint = "buildings/defense/wall_gate_crystal_lvl_2"
}

// All this stuff is just lua, so you can call and execute functions to extract data
function GetSignature()
    return "BuildingComponent,HealthComponent"
end

// Find all entities with BuildingComponent,HealthComponent
local predicate = {
    signature = GetSignature(),
}
```  