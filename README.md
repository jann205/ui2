## Put this to make ui lib working
```lua
_ui = "ohhahtuhthttouttpwuttuaunbotwo"
```
## Loadstring
```lua
local ui = loadstring(game:HttpGet("https://raw.githubusercontent.com/jann205/1/refs/heads/main/ui%20lib.lua", true))()
```
## Creating Window
```lua
local Window = ui:Window({
	ScriptName = "UI HUB",
	DestroyIfExists = true, --if false, gui wont disappear
	Theme = "Dark" --Themes: Pink, White, Dark
})
```
## Creating Close Button
```lua
Window:Close({
	visibility = true, --if false, close button will disappear
	Callback = function()
		Window:Destroy() --Destroying Gui Function
	end,
})
```
## Creating Minimize Button
```lua
Window:Minimize({
	visibility = true, --if false, close button will disappear
	OpenButton = true, -- Visible = false etc, open button.
	Callback = function()
	end,
})
```
## Creating Tab
```lua
local tab1 = Window:Tab("Tab") 
```
## Creating Section
```lua
local newsec = tab1:Section("Section")
```
## Creating Label
```lua
local label = newsec:Label("New Label","Example Description") 
```
## Creating Button
```lua
local button = newsec:Button("New Button","Example Description",function()
	print("Button")
end)
```
## Creating Toggle
```lua
local toggleee = newsec:Toggle("Example Toggle",function(value)
	if value == true then
		print("Activated!")
	elseif value == false then
		print("Disabled!")
	end
end)
```
## Creating Paragraph
```lua
newsec:Paragraph("Paragraph Title",{"Hawk HUB on top","This is a text","Hello again","Mechanism"})
```
## Creating Slider
```lua
local slider = newsec:Slider("Slider Title",16,100,function(value)
	print(value)
end)
```
## Set Slider Value
```lua
slider:SetValue(100)
```
## Creating Line
```lua
newsec:Line()
```
## Creating KeyBind
```lua
newsec:KeyBind("Example Key Bind","Q",function()
	Hawk:ToggleUI() --Toggle UI
end)
```
## Creating TextBox
```lua
newsec:TextBox("Example TextBox","write here",function(value)
	print(value)
end)
```
## Creating Dropdown
```lua
local dropdown = newsec:Dropdown("Example Dropdown",{"Hanki"},function(xd)
	if xd == "Hanki" then
		print("helo")
	end
end)
```
