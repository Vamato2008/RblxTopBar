# RblxTopBar v0.0.2 #

Roblox tool to easily create image buttons on the top bar!<br>
Still in development with future updates and bugs to fix!
<br>

# Getting started

**Roblox model** - TopBar is available in the Roblox asset store for free! You can the model through this link:<br>

https://www.roblox.com/library/9517909355/


**.rbxm file** - Head over to [Releases](https://github.com/Vamato2008/RblxTopBar/releases) page on GitHub, choose the version and download the `.rbxm` file.

<br>

# How to use

You can go to the [docs page](docs) and read the instructions of all the versions.

## Newest version (v0.0.2)

Since in this version I rework the entire module, the creating a button is now done by the following code:
```lua
local module = require(script.TopBar) --require the module
local button = module.new(
   {  --parameters
      ["Name"] = "Name", --button name
      ["IconId"] = 0, --icon id
   }
)
```
The button object has the following functions:
```lua
button:resizeIcon(size:Udim2) --set the icon size
button:resetSize() --reset the icon size to default
button:setIconId(id:number) --set the icon id
```
Finally you can connect some events to the button!
```lua
button.Hover:connect(function()
   --on Hover function
end)

button.UnHover:connect(function()
   --on UnHover function
end)

button.Click1:connect(function()
   --MouseButton1 click event
end)

button.Click2:connect(function()
   --MouseButton2 click event
end)
```
Code examples are available in the [documentation page](docs/Version002.md).