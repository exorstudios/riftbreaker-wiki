---
layout: default
title: Error explanation
nav_order: 2
parent: Debugging
grand_parent: Modding files
---

# Information
This page intends to list the different errors you can get and learn what they actually mean.  
Errors are found in the log files - you can find them in  
`C:\Users\[USERNAME]\Documents\The Riftbreaker\exor_logs.txt`

# Errors

<table>
    <tr>
        <th>Error</th>
        <td>GuiImage.cpp:49 - EXOR_ASSERT( Error: invalid material: gui/hud/XYZ_icon )</td>
    </tr>
    <tr>
        <th>Explanation</th>
        <td>Wrong file name or wrong file path reference inside a file</td>
    </tr>
    <tr>
        <th>Note </th>
        <td>Each texture (even gui) requires a material file</td>
    </tr>
</table>