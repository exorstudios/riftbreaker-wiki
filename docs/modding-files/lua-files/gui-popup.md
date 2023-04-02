---
layout: default
title: Gui popup
nav_order: 92
parent: Lua files
grand_parent: Modding files
---

# Information
Lua can create Gui popups and use button events to make stuff happen, depending on which button is pressed.

# Code example
```lua
function day_cycle_machine:ShowEventPopup()

	GuiService:OpenPopup(self.entity, "gui/popup/popup_template_1button", '<style="header_35">A random event just happened</style>\r\nEvent kind:<style="big_red"> Negative</style>\r\nRiggs just broke a servo reducing his walking speed by 30%')
	self:RegisterHandler(self.entity, "GuiPopupResultEvent", "OnGuiPopupResultEvent")

end


function day_cycle_machine:OnGuiPopupResultEvent( evt )

	if ( evt:GetResult() == "button_ok" ) then
		ConsoleService:Write("Ok!")
	end
	self:UnregisterHandler(evt:GetEntity(), "GuiPopupResultEvent", "OnGuiPopupResultEvent")
end
```

# Explanation
The popup code is separated in 2 functions,  
the **ShowEventPopup()** and the **OnGuiPopupResultEvent( evt )**. 

## ShowEventPopup()
Here we use the actual Gui. Using the lua service `GuiService:OpenPopup`, we can define the responsible entity, the Gui template used and the text.  
The entity is most of the time `self.entity` as the popup is for this entity itself. The template is a path in the Riftbreaker folders.  
The text is what appears on the Gui. It can be styled in certain ways, for more information see gui styling.  
Finally, it creates a [RegisterHandler](../events-requests-registerhandler/#registerhandler) for a popup result event.

## OnGuiPopupResultEvent( evt )
This function gets triggered as soon as the player clicks a button shown on the Gui.
Using the [event](../events-requests-registerhandler/#events) methods, it checks for a button has been pressed on the Gui and performs an action based on that button, in this case an output to the console saying "Ok!"  
Some Gui templates have more than one button, f.e "Yes" + "No", so based on player choice, an action can be performed.  
At the end of the function, the [RegisterHandler](../events-requests-registerhandler/#registerhandler) gets removed.

# Button names
To get the correct naming of the button, for use in the `evt:GetResult()`, use the Gui editor and open the Gui template you chose - on the right you find the name of the button.  
![](../../../../assets/images/gui_editor_button_name.png)