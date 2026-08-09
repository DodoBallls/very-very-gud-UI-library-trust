# 🚀 Very Very Gud UI Library

<p align="center">
  <strong>A simple Roblox UI library with a boot-up animation and reusable window template.</strong>
</p>

<p align="center">
  <a href="https://github.com/DodoBallls/very-very-gud-UI-library-trust">
    <img src="https://img.shields.io/badge/Roblox-Luau-blue?style=for-the-badge" alt="Roblox">
  </a>
  <img src="https://img.shields.io/badge/UI%20Library-Very%20Very%20Gud-purple?style=for-the-badge" alt="UI Library">
  <img src="https://img.shields.io/badge/Mobile-Friendly-green?style=for-the-badge" alt="Mobile Friendly">
</p>

---

## ✨ Features

- 🚀 **Booting Up animation**
- 🪟 **CreateWindow template**
- 🔘 **CreateButton template**
- 🎨 Dark and simple interface
- 📱 Mobile-friendly
- 🧩 Easy API
- ⚡ Minimal setup

---

# 📦 Installation

You only need the **Booting Up** library.

### 🔗 Booting Up

👉 **[Open Booting Up](https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up)**

The Booting Up file contains:

- The boot-up animation
- The `CreateWindow()` template
- The UI window functionality
- The button template

---

# 🚀 Quick Start

Load the library:

```lua
local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()
```

The library will play its boot-up animation.

After the library loads, create your window:

```lua
local Window = Library:CreateWindow("My UI")
```

Then add a button:

```lua
Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)
```

---

# 🪟 Creating a Window

The `CreateWindow()` template is already included inside **Booting Up**.

You do **not** need to manually create a `ScreenGui`, `Frame`, title, or layout.

Simply use:

```lua
local Window = Library:CreateWindow("My UI")
```

### Syntax

```lua
Library:CreateWindow("Window Name")
```

### Example

```lua
local Window = Library:CreateWindow("My Awesome UI")
```

The function returns a `Window` object.

You can then use that object to add UI elements.

---

# 🔘 Creating a Button

Create a button with:

```lua
Window:CreateButton("HiExample", 1, function()
    print("HiExample clicked!")
end)
```

### Syntax

```lua
Window:CreateButton(Name, Order, Callback)
```

### Parameters

| Parameter | Description |
|---|---|
| `Name` | Text displayed on the button |
| `Order` | Position/order of the button |
| `Callback` | Function that runs when clicked |

### Example

```lua
Window:CreateButton("Say Hello", 1, function()
    print("Hello!")
end)
```

You can create as many buttons as you want:

```lua
Window:CreateButton("Button 1", 1, function()
    print("Button 1")
end)

Window:CreateButton("Button 2", 2, function()
    print("Button 2")
end)

Window:CreateButton("Button 3", 3, function()
    print("Button 3")
end)
```

---

# 🧠 How It Works

The library is structured like this:

```text
Your Script
     │
     ▼
Booting Up Library
     │
     ├── 🚀 Boot Animation
     │
     └── 🪟 CreateWindow() Template
              │
              ▼
     Library:CreateWindow("My UI")
              │
              ▼
           Window
              │
              ├── 🔘 CreateButton()
              ├── 🔘 CreateButton()
              └── 🔘 More Elements
```

### Important

**Booting Up does NOT automatically create your window.**

It only provides the `CreateWindow()` template.

You decide what the window is called and when it gets created:

```lua
local Window = Library:CreateWindow("My UI")
```

---

# 🧪 Complete Example

Here is a complete starter script:

```lua
local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()

-- Create the window
local Window = Library:CreateWindow("My UI")

-- Create buttons
Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)

Window:CreateButton("Test", 2, function()
    print("Test clicked!")
end)

Window:CreateButton("Another Button", 3, function()
    print("Another button clicked!")
end)
```

---

# 📋 API Reference

## 🪟 Window

```lua
local Window = Library:CreateWindow("My UI")
```

### Parameters

| Parameter | Type | Description |
|---|---|---|
| `Name` | String | Window title |

---

## 🔘 Button

```lua
Window:CreateButton("Button Name", 1, function()
    print("Clicked!")
end)
```

### Parameters

| Parameter | Type | Description |
|---|---|---|
| `Name` | String | Button text |
| `Order` | Number | Button position |
| `Callback` | Function | Code executed when clicked |

---

# 📁 Library Structure

```text
Very Very Gud UI Library
│
└── Booting Up
    │
    ├── 🚀 Boot Animation
    │
    └── 🪟 CreateWindow()
         │
         └── 🔘 CreateButton()
```

---

# 🛠️ Planned Features

- [ ] 🔄 Toggle
- [ ] 🎚️ Slider
- [ ] 📝 Textbox
- [ ] 📑 Tabs
- [ ] 📂 Sections
- [ ] 🔔 Notifications
- [ ] 🎨 Themes
- [ ] ✨ More animations

---

# 🔗 Source

### Booting Up

**[View Booting Up Source](https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up)**

---

# ❤️ Thanks

Thanks for using **Very Very Gud UI Library**!

More components and features will be added over time.

<p align="center">
  ⭐ Star the repository if you enjoy the library!
</p>