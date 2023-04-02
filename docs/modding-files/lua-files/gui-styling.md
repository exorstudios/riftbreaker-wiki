---
layout: default
title: Gui styling
nav_order: 91
parent: Lua files
grand_parent: Modding files
---

# Information
Besides the normal writing of text, f.e "Hello my name is Tony" in a default way, we can use Riftbreaker styles to change the text appearance.

# Styles library
Riftbreaker has a style library which can be used to change the text appearance, it can be found in: `\Riftbreaker\packs\startup\00_win_startup\gui\styles.kvp`  
It is currently **NOT** possible to edit that file, as it is already parsed before even mods are loaded.  
Each paragrape starts with the style name and in brackets the settings of the style, which defines the style used. 

# Using styles
To use a style, use `<style="STYLE_NAME"> TEXT TEXT TEXT </style>`. Like this, the text in the middle gets affected by the style font you chose.  
The style name is the title of the paragraph found in the styles.kvp.  
Example for "header_35":  
![](../../../../assets/images/gui_styling_header_35.png)  
Multiple can be combined in one text if the text style should change throughout the Gui.

# Style example

You can start a new line with "\r\n"
{: .highlight}

## Normal
```lua
GuiService:OpenPopup(self.entity, "gui/popup/popup_template_1button", '<style="header_35">A random event just happened</style>\r\nEvent kind:<style="big_red"> Negative</style>\r\nRiggs just broke a servo reducing his walking speed by 30%')
```
## As a variable for "Negative"
```lua
local eventKind = " Negative"

GuiService:OpenPopup(self.entity, "gui/popup/popup_template_1button", '<style="header_35">A random event just happened</style>\r\nEvent kind:<style="big_red">' .. eventKind .. '</style>\r\nRiggs just broke a servo reducing his walking speed by 30%')	
self:RegisterHandler(self.entity, "GuiPopupResultEvent", "OnGuiPopupResultEvent")
```  
Both variants of that code look like this in game:  
![](../../../../assets/images/gui_styling_example_1.png)  

## With an image
```lua
local eventKind = " Positive"

GuiService:OpenPopup(self.entity, "gui/popup/popup_template_1button", '<style="header_35">A random event just happened</style>\r\nEvent kind:<style="big_green">' .. eventKind .. '</style>\r\nMr.Riggs stomped into a hole and found a hidden stash with 1500 carbonium<img="gui/hud/resource_icons/carbonium_bigger">')	
self:RegisterHandler(self.entity, "GuiPopupResultEvent", "OnGuiPopupResultEvent")
```
Looks like this in game:  
![](../../../../assets/images/gui_styling_example_2.png)  