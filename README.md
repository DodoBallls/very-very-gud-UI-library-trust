# 🌟 Very Very Gud UI Library

A lightweight Roblox UI library with a built-in boot animation, draggable windows, scrolling, buttons, toggles, and sliders.

## ✨ Features

- 🚀 Booting Up animation
- 🪟 Built-in Window template
- 📱 Mobile friendly
- 🖱️ Mouse dragging
- 👆 Touch dragging
- 📜 Scrolling content
- ♾️ Multiple UI elements
- ➖ Minimize / restore
- ✨ Button animations
- 🔄 Toggle template
- 🎚️ Slider template
- ↔️ Automatic Window resizing
- 📝 Long text support
- 🔢 Element ordering
- 🎨 Rounded UI
- ⚡ Simple API

---

## 📦 Load The Library

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"))()
```

The **Booting Up** file contains the library itself.

When it loads, the boot animation plays automatically.

---

## 🚀 Booting Up

The library automatically displays the boot screen before returning the library.

```text
┌─────────────────────────┐
│      Booting up...      │
│                         │
│ ██████████████████████  │
└─────────────────────────┘
```

You do not need to manually create or start the boot animation.

---

## 🪟 Create A Window

The Window template is already inside the library.

Create one from your outside script:

```lua
local Window = Library:CreateWindow("My UI")
```

You don't need to create a `ScreenGui`, `Frame`, scrolling area, or Window yourself.

---

## 🔘 Button

Create a button:

```lua
Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)
```

### Syntax

```lua
Window:CreateButton(Name, Order, Callback)
```

### Example

```lua
Window:CreateButton("Test Button", 1, function()
    print("Button clicked!")
end)
```

Buttons include:

- Hover animation
- Press animation
- Rounded corners
- Custom text
- Custom order
- Callback

---

## 🔄 Toggle

Create a toggle:

```lua
Window:CreateToggle("Enabled", 2, false, function(Value)
    print(Value)
end)
```

### Syntax

```lua
Window:CreateToggle(Name, Order, Default, Callback)
```

### Example

```lua
Window:CreateToggle("Enabled", 2, false, function(Value)

    if Value then
        print("Enabled")
    else
        print("Disabled")
    end

end)
```

The callback receives either:

```lua
true
```

or:

```lua
false
```

---

## 🎚️ Slider

Create a slider:

```lua
Window:CreateSlider("Speed", 3, 0, 100, 50, function(Value)
    print(Value)
end)
```

### Syntax

```lua
Window:CreateSlider(Name, Order, Min, Max, Default, Callback)
```

### Example

```lua
Window:CreateSlider(
    "Speed",
    3,
    0,
    100,
    50,
    function(Value)
        print("Speed:", Value)
    end
)
```

The slider supports mouse and touch input.

---

## 📜 Scrolling

The Window automatically uses a scrolling content area.

You can add as many elements as you want:

```lua
Window:CreateButton("Button 1", 1)
Window:CreateButton("Button 2", 2)
Window:CreateButton("Button 3", 3)
Window:CreateButton("Button 4", 4)
Window:CreateButton("Button 5", 5)
Window:CreateButton("Button 6", 6)
Window:CreateButton("Button 7", 7)
Window:CreateButton("Button 8", 8)
Window:CreateButton("Button 9", 9)
Window:CreateButton("Button 10", 10)
```

Once the content is larger than the Window, it can be scrolled.

---

## ↔️ Automatic Window Width

The library supports long element names.

Short text:

```lua
Window:CreateButton("Hello", 1)
```

Long text:

```lua
Window:CreateButton(
    "This is a very long button name",
    2
)
```

The Window automatically adjusts its width so the text can be seen.

The width is limited so extremely long text doesn't make the Window enormous.

---

## 🖱️ Dragging

The Window can be dragged using the top bar.

Supported input:

- 🖱️ Mouse
- 📱 Touch

No extra dragging code is required.

---

## ➖ Minimize / Restore

The Window has a minimize button in the top-left corner.

Press:

```text
−
```

to minimize it.

Press:

```text
+
```

to restore it.

Both actions use smooth TweenService animations.

---

## 📱 Mobile Support

The library is designed to work with mobile devices.

Supported:

- Touch dragging
- Touch scrolling
- Touch sliders
- Mobile buttons
- Compact Window layout

---

## 🔢 Element Ordering

The second parameter determines the order of the elements.

```lua
Window:CreateButton("First", 1)

Window:CreateToggle("Second", 2, false)

Window:CreateSlider("Third", 3, 0, 100, 50)
```

The result is:

```text
First
Second
Third
```

You can mix buttons, toggles, and sliders.

---

## 📚 API

### CreateWindow

```lua
Library:CreateWindow(Name)
```

### CreateButton

```lua
Window:CreateButton(Name, Order, Callback)
```

### CreateToggle

```lua
Window:CreateToggle(Name, Order, Default, Callback)
```

### CreateSlider

```lua
Window:CreateSlider(Name, Order, Min, Max, Default, Callback)
```

---

## 🧩 Complete Example

```lua
local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()

local Window = Library:CreateWindow("My UI")

Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)

Window:CreateButton("Another Button", 2, function()
    print("Another button!")
end)

Window:CreateToggle("Enabled", 3, false, function(Value)
    print("Enabled:", Value)
end)

Window:CreateSlider(
    "Speed",
    4,
    0,
    100,
    50,
    function(Value)
        print("Speed:", Value)
    end
)
```

---

## ⚠️ Important

The elements belong to the Window.

### ✅ Correct

```lua
Window:CreateButton("Button", 1)
```

```lua
Window:CreateToggle("Toggle", 2, false)
```

```lua
Window:CreateSlider("Slider", 3, 0, 100, 50)
```

### ❌ Incorrect

```lua
Library:CreateButton("Button", 1)
```

The `Library` creates Windows.

The `Window` creates the elements.

---

## 🏠 Basic Structure

```text
Your Script
│
├── Load Booting Up
│
├── Create Window
│
├── Create Button
│
├── Create Toggle
│
└── Create Slider
```

In code:

```lua
local Library = loadstring(game:HttpGet("BOOTING UP URL"))()

local Window = Library:CreateWindow("My UI")

Window:CreateButton(...)
Window:CreateToggle(...)
Window:CreateSlider(...)
```

---

## ⚡ Quick Start

Copy this:

```lua
local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()

local Window = Library:CreateWindow("My UI")

Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)
```

---

## 🌟 Very Very Gud UI Library

**Boot → Window → Elements → Done.**