# STREET RACER

A 3D arcade racing game written in C with [raylib](https://www.raylib.com/).

## Features
- Driver profile, main menu, settings and pause screen
- One-way / two-way traffic and three difficulty levels
- Four selectable player vehicles and mixed traffic
- Procedural 3D road scene, HUD, nitro and horn

## Controls
- Steer: A / D or Left / Right arrows
- Accelerate: W / Up arrow
- Brake: S / Down arrow
- Nitro: Space
- Horn: H
- Pause: P / Escape
- Retry after a crash: R

## Build on macOS
Install CMake and raylib. First decode the source archive, then build:

```sh
base64 -D -i source.zip.b64 -o source.zip
cmake -S . -B build
cmake --build build --config Release
./build/STREET_RACER
```

CMake extracts the original `main.c` from `source.zip` automatically.

## Windows build
Every push to `main` triggers the GitHub Actions workflow. Open the repository's **Actions** tab, select the successful **Build Windows Game** run, and download the `STREET-RACER-Windows` artifact. It contains `STREET_RACER.exe`.

The Windows workflow uses vcpkg's static Raylib triplet and decodes the source archive automatically.
