---
layout: default
title: Accessing keyboard hotkeys
nav_order: 93
parent: Lua files
grand_parent: Modding files
---

# Information
This is currently a workaround version of accessing the hotkeys via code. EXOR plans to add a better way in the future.

# Code example
```lua
ConsoleService:RegisterCommand( "activate_slot_request", function( args )
    if not Assert( #args == 1, "Command requires one argument! [slot_name]" ) then return end   

    ItemService:UseEquippedItem(PlayerService:GetPlayerControlledEnt(0),args[1])
end)

ConsoleService:ExecuteCommand('bind f1 "activate_slot_request USABLE_9"')
```

# Keyboard key codes
```qml
backspace = KEY_BACKSPACE;
tab = KEY_TAB;
escape = KEY_ESCAPE;
space = KEY_SPACE;
page_up = KEY_PAGE_UP;
page_down = KEY_PAGE_DOWN;
end = KEY_END;
home = KEY_HOME;
left = KEY_LEFT;
up = KEY_UP;
right = KEY_RIGHT;
down = KEY_DOWN;
num_0 = KEY_NUMPAD0;
num_1 = KEY_NUMPAD1;
num_2 = KEY_NUMPAD2;
num_3 = KEY_NUMPAD3;
num_4 = KEY_NUMPAD4;
num_5 = KEY_NUMPAD5;
num_6 = KEY_NUMPAD6;
num_7 = KEY_NUMPAD7;
num_8 = KEY_NUMPAD8;
num_9 = KEY_NUMPAD9;
select = KEY_SELECT;
return = KEY_RETURN;
insert = KEY_INSERT;
delete = KEY_DELETE;
0 = KEY_0;
1 = KEY_1;
2 = KEY_2;
3 = KEY_3;
4 = KEY_4;
5 = KEY_5;
6 = KEY_6;
7 = KEY_7;
8 = KEY_8;
9 = KEY_9;
a = KEY_A;
b = KEY_B;
c = KEY_C;
d = KEY_D;
e = KEY_E;
f = KEY_F;
g = KEY_G;
h = KEY_H;
i = KEY_I;
j = KEY_J;
k = KEY_K;
l = KEY_L;
m = KEY_M;
n = KEY_N;
o = KEY_O;
p = KEY_P;
q = KEY_Q;
r = KEY_R;
s = KEY_S;
t = KEY_T;
u = KEY_U;
v = KEY_V;
w = KEY_W;
x = KEY_X;
y = KEY_Y;
z = KEY_Z;
* = KEY_MULTIPLY;
+ = KEY_ADD;
- = KEY_SUBTRACT;
. = KEY_DECIMAL;
/ = KEY_DIVIDE;
f1 = KEY_F1;
f2 = KEY_F2;
f3 = KEY_F3;
f4 = KEY_F4;
f5 = KEY_F5;
f6 = KEY_F6;
f7 = KEY_F7;
f8 = KEY_F8;
f9 = KEY_F9;
f10 = KEY_F10;
f11 = KEY_F11;
f12 = KEY_F12;
f13 = KEY_F13;
f14 = KEY_F14;
f15 = KEY_F15;
f16 = KEY_F16;
f17 = KEY_F17;
f18 = KEY_F18;
f19 = KEY_F19;
f20 = KEY_F20;
f21 = KEY_F21;
f22 = KEY_F22;
f23 = KEY_F23;
f24 = KEY_F24;
lshift = KEY_LSHIFT;
rshift = KEY_RSHIFT;
lcontrol = KEY_LCONTROL;
rcontrol = KEY_RCONTROL;
lmenu = KEY_LMENU;
rmenu = KEY_RMENU;
lalt = KEY_LMENU;
ralt = KEY_RMENU;
dpad_up = KEY_PAD_DPAD_UP;
dpad_down = KEY_PAD_DPAD_DOWN;
dpad_right = KEY_PAD_DPAD_RIGHT;
dpad_left = KEY_PAD_DPAD_LEFT;
pad_a = KEY_PAD_A;
pad_b = KEY_PAD_B;
pad_c = KEY_PAD_C;
pad_x = KEY_PAD_X;
pad_y = KEY_PAD_Y;
pad_z = KEY_PAD_Z;
pad_start = KEY_PAD_START;
pad_back = KEY_PAD_BACK;
pad_mode = KEY_PAD_MODE;
pad_rthumb = KEY_PAD_RIGHT_THUMB;
pad_lthumb = KEY_PAD_LEFT_THUMB;
rs = KEY_PAD_RIGHT_SHOULDER;
ls = KEY_PAD_LEFT_SHOULDER;
rt = KEY_PAD_RIGHT_TRIGGER;
lt = KEY_PAD_LEFT_TRIGGER;
mr = KEY_MOUSE_RIGHT;
ml = KEY_MOUSE_LEFT;
m3 = KEY_MOUSE_MIDDLE;
m4 = KEY_MOUSE_XBUTTON1;
m5 = KEY_MOUSE_XBUTTON2;
```