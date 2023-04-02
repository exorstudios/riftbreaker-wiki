---
layout: default
title: Crash explanation
nav_order: 3
parent: Debugging
grand_parent: Modding files
---

# Information
This page intends to list the different crashes you can get and learn what they actually mean.  
Every crash logs some information at the end of the log files - you can find them in  
`C:\Users\[USERNAME]\Documents\The Riftbreaker\exor_logs.txt`

# Crashes

<table>
    <tr>
        <th>Crash</th>
        <td>(filename not available):0 - public: void * __ptr64 __cdecl Exor::CompContainer::GetComponent(enum Exor::TypeHash) __ptr64</td>
    </tr>
    <tr>
        <th>Explanation</th>
        <td>Wrong file name or wrong file path reference inside a file</td>
    </tr>
    <tr>
        <th>Example </th>
        <td>example_name.ent file is located in "buildings/main/example_name" but in the entity file it says "buildings/defense/example_name" as the blueprint name</td>
    </tr>
</table>

---

<table>
    <tr>
        <th>Crash</th>
        <td>(filename not available):0 - Exor::CompContainer::GetComponent</td>
    </tr>
    <tr>
        <th>Explanation</th>
        <td>Missing value for variable in entity file</td>
    </tr>
    <tr>
        <th>Example </th>
        <td>The variable "ammo_blueprint" being " ". Instead of nothing, something should be written - like "buildings/defense/tower_alien_influence/spawner"</td>
    </tr>
</table>