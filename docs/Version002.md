# Version 0.0.2 documentation

**You must use this version in the client side.**

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
<hr>

## Code examples

Button that prints a message when clicked:
```lua
local module = require(script.TopBar) --require the module
local button = module.new(
   {
      ["Name"] = "Name",--button name
      ["IconId"] = 0,   --icon id
   }
)
button.Click1:connect(function()
   print("Button clicked!")
end)
```
Icon changing on hover:
```lua
local module = require(script.TopBar) --require the module
local button = module.new(
   {
      ["Name"] = "Name",--button name
      ["IconId"] = 0,   --icon id
   }
)

button.Hover:connect(function()
   button:setIconId(1)
end)

button.UnHover:connect(function()
   button:setIconId(0)
end)
```
Changing the button size  randomly on click:
```lua
local module = require(script.TopBar) --require the module
local button = module.new(
   {
      ["Name"] = "Name",--button name
      ["IconId"] = 0,   --icon id
   }
)

button.Click1:connect(function()
   button:resizeIcon(UDim2.fromOffset(
      math.random(10,50),
      math.random(10,50)
      )
   )
end)
```