# Revenant Modded UI Library

# Updates Weekly/Daily  
# simple, fast, and flexible UI for scripts

A customizable **Modified UI library for Roblox** focused on creating script interfaces:
windows, buttons, toggles, sliders, dropdowns, keybinds, and notifications — with minimal setup.

Designed to be **easy to drop in**, visually clean, and extensible.

---

# Quick Install

```lua
local Revenant = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/ofugii/Revenant-Modded/refs/heads/main/source.lua"
))()
```

---

# Minimal Example

```lua
local Revenant = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/ofugii/Revenant-Modded/refs/heads/main/source.lua"
))()

local Window = Revenant:Window({
    Text = "Revenant UI"
})

Window:Button({
    Text = "Hello",
    Callback = function()
        print("Hello world")
    end
})

Revenant:Notification({
    Text = "UI Loaded",
    Duration = 3
})
```

---

# Full Example

```lua
local Revenant = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/ofugii/Revenant-Modded/refs/heads/main/source.lua"
))()

-- main window
local Window = Revenant:Window({
    Text = "Settings",
    Center = true
})

-- button
Window:Button({
    Text = "Print Test",
    Callback = function()
        print("Button clicked")
    end
})

-- toggle
Window:Toggle({
    Text = "Enable Feature",
    Default = false,
    Callback = function(state)
        print("Feature:", state)
    end
})

-- slider
Window:Slider({
    Text = "Volume",
    Minimum = 0,
    Maximum = 100,
    Default = 50,
    Postfix = "%",
    Callback = function(value)
        print("Volume:", value)
    end
})

-- dropdown
Window:Dropdown({
    Text = "Mode",
    List = {"Easy", "Normal", "Hard"},
    Callback = function(choice)
        print("Mode:", choice)
    end
})

-- keybind
Window:Keybind({
    Text = "Toggle UI",
    Default = Enum.KeyCode.RightControl,
    Callback = function()
        Revenant:Toggle()
    end
})

-- notification
Revenant:Notification({
    Text = "Everything loaded successfully",
    Duration = 4
})
```

---

# Setup (Optional)

```lua
Revenant:Setup({
    Theme = "Dark",
    Font = Enum.Font.Gotham
})
```

---

# Elements

## Window
```lua
local Window = Revenant:Window({
    Text = "Window Title"
})
```

## Button
```lua
Window:Button({
    Text = "Click Me",
    Callback = function() end
})
```

## Toggle
```lua
Window:Toggle({
    Text = "Enable",
    Default = false,
    Callback = function(state) end
})
```

## Slider
```lua
Window:Slider({
    Text = "Value",
    Minimum = 0,
    Maximum = 100,
    Default = 25,
    Callback = function(value) end
})
```

## Dropdown
```lua
Window:Dropdown({
    Text = "Select",
    List = {"A", "B", "C"},
    Callback = function(choice) end
})
```

## Keybind
```lua
Window:Keybind({
    Text = "Toggle UI",
    Default = Enum.KeyCode.LeftControl,
    Callback = function() end
})
```

## Notification
```lua
Revenant:Notification({
    Text = "Notification text",
    Duration = 3
})
```

---

# Control

```lua
Revenant:Toggle()   -- show / hide UI
Revenant:Destroy()  -- remove UI completely
```

---

# Module Install

```lua
local Revenant = require(path.to.Revenant)

Revenant:Window({ Text = "Hello" })
```

---

# Notes

• Designed for exploit's or local UI environments  
• This is Open Source But please put Creduts please and Thank you!
---

# GitHub

https://github.com/ofugii/Revenant-Modded
