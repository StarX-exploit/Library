This Script Is Beta And Idk Just use it, my friend give me the source. 

# Booting The Library
```
local lib = loadstring(game:HttpGet("https://raw.githubusercontent.com/StarX-exploit/Library/refs/heads/main/Main.lua"))()
```
# Label
```
local window = lib:CreateWindow("Star X")
```
# Button
```
local button = lib:CreateButton(window, "Print Text", function()
    print("Hello World")
end)
```
# Text Box
```
local textBox = lib:CreateTextBox(window, Enum.Font.Legacy, "Text", "Hello, World!")
```
# Dropdown
```
lib:NewDropdownButton(window, drop, "Print 'LOL'", function()
   print("LOL") 
```
# DropdownButton
```
lib:NewDropdownButton(window, drop, "Print 'YES'", function()
   print("YES")
end)
```
# Slider
```
local slider = lib:CreateSlider(window, "Print Value", 0, 100, 50, function(value)
    print(value)
end)
```
# Keybind
```
local keybind = lib:CreateKeyBind(window, "Print Key", "z", function(key)
    print(key)
end)
```


# EXAMPLE
```
local lib = loadstring(game:HttpGet("https://raw.githubusercontent.com/StarX-exploit/Library/refs/heads/main/Main.lua"))()
local window = lib:CreateWindow(" Your Hub")
local label = lib:CreateLabel(window, "Main")
local textBox = lib:CreateTextBox(window, Enum.Font.Legacy, "Text", "Hello, World!")

local button = lib:CreateButton(window, "Print Text", function()
    print(textBox.Text)
end)

local toggled = false
local toggle = lib:CreateToggle(window, "Spam Warn 'Hello'", false, function(toggleState)
    toggled = not toggled
    while toggled and game:GetService('RunService').Heartbeat:Wait() do
        warn("Hello")
    end
end)

local drop = lib:CreateDropdown(window, "Dropdown")
lib:NewDropdownButton(window, drop, "Print 'LOL'", function()
   print("LOL")
end)

lib:NewDropdownButton(window, drop, "Print 'YES'", function()
   print("YES")
end)

lib:NewDropdownButton(window, drop, "Warn 'XD'", function()
   warn("XD")
end)

local slider = lib:CreateSlider(window, "Print Value", 0, 100, 50, function(value)
    print(value)
end)

local keybind = lib:CreateKeyBind(window, "Print Key", "z", function(key)
    print(key)
end)
```
