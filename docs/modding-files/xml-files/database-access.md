---
layout: default
title: Database access 
nav_order: 3
parent: XML files
grand_parent: Modding files
---

# Information

XML files can create a database which can be accessed by Lua files.
The database has to be created by declaring a typical key-value field.

# Database data types

| Data type        | XML-Code     |
|:-------------:|:--------------:|
| String | database.Strings.StringData[0].key |
| Int | database.Integers.IntData[0].key |
| Float | database.Floats.FloatData[0].key |

Each entry for the same data type has to use the next number.
First string would be `database.Strings.StringData[0].key` the next string would be  
`database.Strings.StringData[1].key` etc.  

# Example

```html
<value id="database.Integers.IntData[0].key" value="instant" />
<value id="database.Floats.FloatData[0].key" value="speed" />
<value id="database.Integers.IntData[1].key" value="instant_fast" />
<value id="database.Strings.StringData[0].key" value="tower_bp"/>
```
  
# Lua
To access these fields in Lua, you would use the normal commands to access the data, example:
```lua
function my_lua_function:init()
    self.my_variable_1 = self.data:GetInt("instant")
    self.my_variable_2 = self.data:GetFloat("speed")
    self.my_variable_3 = self.data:GetInt("instant_fast")
    self.my_variable_4 = self.data:GetString("tower_bp")
end
```
The value in the brackets, like ("speed") is the **value** from the database key-value field above. 