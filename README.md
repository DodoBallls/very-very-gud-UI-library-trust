🚀 Very Very Gud UI Library

A simple Roblox UI library with a built-in Booting Up animation and a reusable Window template.

📦 Booting Up

The only library file you need is Booting Up.

It contains:

- ⚡ Boot-up animation
- 🪟 "CreateWindow()" template
- 🔘 "CreateButton()" template

🔗 Booting Up

"Booting Up Library" (https://reference-url-citation.invalid/0)

---

⚡ Quick Start

Load the library:

local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()

After the boot animation finishes, create your window:

local Window = Library:CreateWindow("My UI")

Then add elements:

Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)

---

🪟 Create a Window

The "CreateWindow()" template is already inside Booting Up.

You only need to call it from your own script:

local Window = Library:CreateWindow("My UI")

Parameters

CreateWindow(Name)

Parameter| Description
"Name"| The title displayed on the window

Example:

local Window = Library:CreateWindow("My Cool UI")

---

🔘 Create a Button

Use:

Window:CreateButton("HiExample", 1, function()
    print("Button clicked!")
end)

Parameters

CreateButton(Name, Order, Callback)

Parameter| Description
"Name"| Button text
"Order"| Button position
"Callback"| Code executed when clicked

Example:

Window:CreateButton("Test", 1, function()
    print("Test clicked!")
end)

---

📋 Complete Example

Copy this entire script:

local Library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/DodoBallls/very-very-gud-UI-library-trust/refs/heads/main/Booting%20Up"
))()

local Window = Library:CreateWindow("My UI")

Window:CreateButton("Hello", 1, function()
    print("Hello!")
end)

Window:CreateButton("Test", 2, function()
    print("Test clicked!")
end)

---

🧠 How It Works

Your Script
     │
     ▼
Booting Up
     │
     ├── Boot animation
     │
     └── CreateWindow() template
              │
              ▼
       Your CreateWindow()
              │
              ▼
            Window
              │
              ├── CreateButton()
              ├── CreateButton()
              └── More elements later

The important part is that Booting Up does not automatically create the window.

You decide when and what window to create:

local Window = Library:CreateWindow("My UI")

---

🔗 Source

Booting Up

"Open Booting Up Source" (https://reference-url-citation.invalid/1)

---

📝 Notes

- Load Booting Up first.
- Wait for its boot animation to finish.
- Use "Library:CreateWindow()" to create your window.
- Use the returned "Window" object to create UI elements.
- "Order" controls the order of elements inside the window.

More UI components can be added to the library later, such as:

- 🔄 Toggles
- 🎚️ Sliders
- 📝 Textboxes
- 📑 Tabs
- 📂 Sections
- 🔔 Notifications
- 🎨 Themes