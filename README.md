# RblxTopBar v0.0.1 #

Roblox tool to easily create image buttons on the top bar!<br>
Still in development with future updates and bugs to fix!
<br><br>

# Getting started

**Roblox model** - TopBar is available in the Roblox asset store for free! You can the model through this link:<br>

https://www.roblox.com/library/9517909355/


**.rbxm file** - Head over to [Releases](https://github.com/Vamato2008/RblxTopBar/releases) page on GitHub, choose the version and download the `.rbxm` file.

<br>

# How to use

First you require the module and create a button object
```lua
local button = require(script.TopBar)()
```
Then you can set button properties using this functions
```lua
local button = require(script.TopBar)()
button.SetIconID(id)
button.Rename(name)
button.ResizeIcon(UDim2.new())
--reset size to default
button.ResetSize()
```
And finally you can connect some functions to the button!
```lua
local button = require(script.TopBar)()
button.Hover:Connect(function()
	--on Hover function
end)
button.UnHover:Connect(function()
	--on UnHover function
end)
button.Clicked1:Connect(function()
	--MouseButton1 click event
end)
button.Clicked2:Connect(function()
	--MouseButton2 click event
end)
```