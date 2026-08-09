✨ Very Very Gud UI Library

<p align="center">
  <strong>A lightweight Roblox UI library with a smooth boot-up animation and simple UI creation.</strong>
</p><p align="center">
  <img src="https://img.shields.io/badge/Roblox-Luau-blue?style=for-the-badge&logo=roblox" alt="Roblox">
  <img src="https://img.shields.io/badge/UI-Library-purple?style=for-the-badge" alt="UI Library">
  <img src="https://img.shields.io/badge/Mobile-Friendly-green?style=for-the-badge" alt="Mobile Friendly">
</p>---

🌟 Features

Feature| Available
🚀 Boot-up animation| ✅
🪟 Window template| ✅
🔘 Buttons| ✅
🎨 Animated UI| ✅
📱 Mobile friendly| ✅
🧩 Easy API| ✅

---

📥 Installation

The library uses Booting Up as its main entry point.

🔗 Booting Up

"Open Booting Up" (https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up)

You only need to load this file.

---

🚀 Quick Start

Paste this into your script:

local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()

local Window = Library:CreateWindow("My UI")

Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)

«💡 Tip: GitHub automatically adds a Copy button to the top-right of code blocks.»

---

🪟 Creating a Window

The "CreateWindow()" template is already included inside Booting Up.

You call it from your own script:

local Window = Library:CreateWindow("My UI")

Syntax

Library:CreateWindow(Name)

Example

local Window = Library:CreateWindow("My Awesome UI")

---

🔘 Buttons

Buttons are created with:

Window:CreateButton("Example", 1, function()
    print("Button clicked!")
end)

📌 Parameters

Parameter| Type| Description
"Name"| String| Button's displayed name
"Order"| Number| Position in the window
"Callback"| Function| Runs when the button is clicked

Example

Window:CreateButton("Say Hello", 1, function()
    print("Hello!")
end)

Window:CreateButton("Test Button", 2, function()
    print("Test!")
end)

---

🧪 Complete Example

Here's a complete starter script:

--// Load Library

local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()

--// Create Window

local Window = Library:CreateWindow("My UI")

--// Create Buttons

Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)

Window:CreateButton("Test", 2, function()
    print("Test clicked!")
end)

Window:CreateButton("Another Button", 3, function()
    print("Another button!")
end)

---

🧠 How The Library Works

                 ┌───────────────────┐
                 │    Your Script    │
                 └─────────┬─────────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │    Booting Up     │
                 │                   │
                 │  🚀 Boot Animation│
                 │  🪟 Window Template│
                 └─────────┬─────────┘
                           │
                           ▼
                 Library:CreateWindow()
                           │
                           ▼
                 ┌───────────────────┐
                 │       Window      │
                 ├───────────────────┤
                 │ 🔘 Button         │
                 │ 🔘 Button         │
                 │ 🔘 Button         │
                 └───────────────────┘

The important part is:

Booting Up contains the templates.

It does not automatically decide what your window should be called.

You decide:

local Window = Library:CreateWindow("My UI")

---

🧩 API

Window

Library:CreateWindow("Window Name")

Button

Window:CreateButton(
    "Button Name",
    1,
    function()
        print("Clicked!")
    end
)

---

🎨 UI Design

The library uses a compact dark interface with:

- Rounded corners
- Animated interactions
- Small mobile-friendly controls
- Draggable window
- Simple API
- Minimal setup

---

📱 Mobile Support

The UI is designed to be usable on smaller screens.

Touch input can be used for interacting with the interface, while the window can be dragged around the screen.

---

🔗 Source

Booting Up

"View Source" (https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up)

---

🛠️ Roadmap

Planned UI components:

- [ ] 🔄 Toggle
- [ ] 🎚️ Slider
- [ ] 📝 Textbox
- [ ] 📑 Tabs
- [ ] 📂 Sections
- [ ] 🔔 Notifications
- [ ] 🎨 Theme system
- [ ] ✨ More animations

---

<p align="center">
  <strong>Made for simple, clean Roblox interfaces ❤️</strong>
</p>