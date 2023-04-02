---
layout: default
title: Node UI styles 
nav_order: 2
parent: XML files
grand_parent: Modding files
---

# Information
When creating a node, the UI is created by using different kinds of XML code.  
The styles here provide an UI overview. 

# UI styles
## List

```html
<list source="blueprints" text="item" filter="items/" width="240" id="database.Strings.StringData[0].value" value="items/weapons/plasma_item" font_weight="bold" />
```

## Input

```html
<input width="240" type="int" text="count" id="database.Integers.IntData[0].value" value="0" font_weight="bold" />
```

## Button

```html
<button value="False"  action="add;condition_false.xml"  width="100"   target="conditions"/>
```