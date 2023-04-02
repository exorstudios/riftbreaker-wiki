---
layout: default
title: Node layouts 
nav_order: 1
parent: XML files
grand_parent: Modding files
---

# Information
XML files use a different kind of node layout, depending on their task.

# Node layouts  

| Node layout name  - XML | Node layout name - Lua | Node purpose |
|:-------------|:--------------|:--------------|
| LuaBehaviourNode | LuaGraphNode | Executes a task  |
| NodeSelectorNode | LuaGraphNodeSelector | Logic node  |

# Lua code differences

<table>
    <tr>
        <th></th>
        <td>Difference 1</td><td>Difference 2</td><td>Difference 3</td>
    </tr>
    <tr>
        <th>LuaBehaviourNode / <br/>LuaGraphNode</th>
        <td>self:SetFinished( ) </td><td>  </td><td>  </td>
    </tr>
    <tr>
        <th>NodeSelectorNode / <br/>LuaGraphNodeSelector</th>
        <td>self:SetFinished( "true" )<br/>self:SetFinished( "false" )</td><td>  </td><td>  </td>
    </tr>
</table>
