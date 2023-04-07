---
title: INTERNAL_STYLING_GUIDE
layout: default
nav_exclude: true
---

# Normal table #  

| Node layout name  - XML | Node layout name - Lua | Node purpose |
|:-------------|:--------------|:--------------|
| LuaBehaviourNode | LuaGraphNode | Executes a task  |
| NodeSelectorNode | LuaGraphNodeSelector | Logic node  |



# Sideways table  #  

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


# Linking pictures #
![](../../../../assets/images/gui_styling_header_35.png)  