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
## Text
### Example
**Doesn't feature all available options**
```html
<text value="Localization:" width="90" font_weight="bold" align="left" />
```
### Options

| - | value | width | font_weight | align |
|:-------------|:-------------|:--------------|:--------------|:--------------|
| Options | Any / No text | Any number | bold, extra_bold  | left, right |
| Explanation | What is shown as pre-selected | Sets the UI width | Styles text | Sets the text alignment |

---

## List
### Example
**Doesn't feature all available options**
```html
<list source="blueprints" text="item" filter="items/" width="240" id="database.Strings.StringData[0].value" value="items/weapons/plasma_item" font_weight="bold" />
```
### Options

| - | source | text | filter | width | id | value | font_weight | delimiter | hide_string | align | not_empty | valid_rule | tooltip | type |
|:-------------|:-------------|:--------------|:--------------|:--------------:|:--------------|
| Options | Any text, Int, Float etc. | Any / No text | ex:<br/>items/ | Any number | ex: database.Strings.StringData[1].value | Any / No text | bold, extra_bold | / | ex:<br/>voice_over/ | left, right | [0,1] | not_empty | Any / No text | selector, multi |
| Explanation | What is available to choose in the Gui. Often used in combination with the Lua file to allow a selection | What text to show | Shows only entries which contain that filter | Sets the UI width | Takes a value from the key-value pair declared top | What is shown as pre-selected | Styles text | Which symbol separates options | Don't show entries which contain that string | Sets the text alignment | Allows / Disallows empty | Checks if a rule condition is met | (Doesn't seem to work currently) | How to choose an entry |

---

## Input
### Example
**Doesn't feature all available options**
```html
<input width="240" type="int" text="count" id="database.Integers.IntData[0].value" value="0" font_weight="bold" />
```
### Options

| - | source | text | width | id | value | font_weight | not_empty | valid_rule | type | min | max | step |
|:-------------|:-------------|:--------------|:--------------|:--------------:|:--------------|
| Options | Any text, Int, Float etc. | Any / No text | Any number | self_id / <br/>ex: database.Strings.StringData[1].value | Any / No text | bold, extra_bold | [0,1] | not_empty | float, int | Any Int | Any Int | Any Int |
| Explanation | What is available to choose in the Gui. Often used in combination with the Lua file to allow a selection | What text to show | Sets the UI width | Sets the id of this input / <br/>Takes a value from the key-value pair declared top | What is shown as pre-selected | Styles text | Allows / Disallows empty | Checks if a rule condition is met | Sets the type of the input box | Sets a minimum allowed input value | Sets a maximum allowed input value | The Int sets the steps in which to increase / decrease the value |

---

## Button
### Example
**Doesn't feature all available options**
```html
<button value="False"  action="add;condition_false.xml"  width="100"   target="conditions"/>
```
### Options

| - | width | value | font_weight | action | target | bgcolor | tooltip |
|:-------------|:-------------|:--------------|:--------------|:--------------:|:--------------|
| Options | Any number | Any / No text | bold, extra_bold | [add + xml-file], <br/> [script + show_translation / play_sound / show_dialog_translation / edit_embedded_script / generate_int_branches / open_graph / update_bindings] | A key-value pair declared top, dialogs, conditions, graph, Enemies | Any hex color | Any / No text |
| Explanation | Sets the button width | What is shown on the button | Styles text | Triggers an action from the "graph_nodes/sub_event" folder <br/>(Can only be seen in the workspace editor) | Action target | Sets button color | (Doesn't seem to work currently) |