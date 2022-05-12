# Version 0.0.1 documentation

**You must use this version in the client side.**

First you require the module and create a button object:
```lua
local button = require(script.TopBar)()
```
Then you can set button properties using this functions:
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
Not much things yet, but I will add more features soon!