---
name: openclaw
description: Use this skill when working with the OpenClaw game engine or its Lua scripting systems. Triggers when modifying engine source code, Lua scripts, or asset configurations.
---

# OpenClaw

## What this is
OpenClaw is an open-source, cross-platform re-implementation of the engine used in the 1997 platformer game "Claw". It is written in C++ and leverages SDL2 to ensure compatibility with modern operating systems while introducing advanced features like Lua scripting for object logic.

## Installation
```bash
git clone https://github.com/OpenClaw/OpenClaw.git
mkdir build && cd build
cmake ..
make
# Note: Requires original CLAW.REZ file in the execution directory
```

## Key concepts
- **REZ Archive**: The engine uses a virtual file system to read assets from original `.REZ` containers. You do not need to extract these files; the engine accesses them directly via internal paths.
- **Lua Logic**: Unlike the original game, OpenClaw uses Lua for level logic and object behaviors. This allows for runtime modification of enemy AI and interactive elements.
- **WAP Maps**: Level layouts are stored in `.WAP` files, which define tile layers, object placement, and logic triggers.
- **SDL2 Rendering**: The engine utilizes SDL2 for hardware-accelerated rendering, allowing for windowed modes and modern resolution scaling.

## Correct usage patterns
- **Lua Scripting for Objects**:
  When defining a new object behavior in a Lua script:
  ```lua
  -- Example: A custom health pickup script
  function OnTouch(player, object)
      if player:GetHealth() < 100 then
          player:AddHealth(10)
          object:Destroy()
          PlaySound("GAME_GETHEALTH")
      end
  end
  ```
- **Configuring the Engine**:
  Adjusting settings via `config.xml`:
  ```xml
  <config>
      <video width="800" height="600" fullscreen="false" vsync="true" />
      <game path="./CLAW.REZ" />
  </config>
  ```

## Common mistakes to avoid
- **Case Sensitivity**: Linux builds are case-sensitive. Ensure that asset paths requested in code match the case inside the `.REZ` file (e.g., `IMAGES/LEVEL1.PCX` vs `images/level1.pcx`).
- **Missing Original Assets**: OpenClaw is an engine only. It will fail to launch without the original `CLAW.REZ` file from the 1997 retail game.
- **Lua Syntax**: Ensure scripts follow the specific Lua version embedded (typically Lua 5.3). Avoid using platform-specific OS calls within Lua scripts to maintain cross-platform compatibility.

## File and folder conventions
- `/src`: Contains the C++ source code for the engine core and rendering logic.
- `/scripts`: Directory for Lua-based object behaviors and level logic.
- `/assets`: Location for external configuration files and non-REZ media.
- `config.xml`: The primary configuration file for engine behavior and asset paths.