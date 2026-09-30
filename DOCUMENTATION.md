# Automatic Light Recognizer — Toggle By Time

A simple Roblox system that automatically turns lights on or off depending on the current time of day.

## 📌 Description

This system detects the current `Lighting.ClockTime` and automatically changes the state of configured lights.

* 🌙 Lights turn **on** during nighttime.
* ☀️ Lights turn **off** during daytime.
* ⚙️ The system checks the time automatically.
* 🧩 Easy to integrate into existing Roblox projects.

## 📂 Structure

```text
Automatic-Light-Recognizer-Toggle-By-Time
│
├── Main.server.lua
└── README.md
```

## ⚙️ How It Works

The system uses `Lighting.ClockTime` to determine whether it is currently day or night.

```lua
local Lighting = game:GetService("Lighting")

if Lighting.ClockTime >= 18 or Lighting.ClockTime <= 6 then
    -- Night
else
    -- Day
end
```

When the current time enters the configured nighttime range, the system enables the lights. When daytime begins, the lights are disabled.

## 🔧 Configuration

You can modify the time range directly in the script.

```lua
local NIGHT_START = 18
local NIGHT_END = 6
```

For example:

```lua
local NIGHT_START = 19
local NIGHT_END = 5
```

This would make the lights activate between **19:00 and 05:00**.

## 🚀 Installation

1. Download or clone this repository.
2. Open your Roblox Studio project.
3. Place the scripts in `ServerScriptService` and also `ReplicatedStorage`.
4. Configure the folder or objects containing the lights if necessary.
5. Run the game and test the system.

## 💡 Requirements

* Light Models
* Add Tag All Light Models (in my case I added the tag in the SpotLights/PointLights)
* Lights compatible with the properties used by the script

## 📝 Notes

This project is intentionally simple and is intended as a small, reusable Roblox system.

Feel free to modify the code to fit your own project.

## 👤 Author

**CrisDev**

Roblox Programmer
