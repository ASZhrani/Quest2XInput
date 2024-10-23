# Meta Quest Controller to Xbox Controller Input Converter

This project is a simple application that converts the input from **Meta Quest 2** and **Meta Quest 3** controllers into **Xbox Controller** inputs. This allows you to use your VR controllers just like an Xbox controller for games and other applications. The program is written in **C++** and uses libraries to communicate with the Meta Quest controllers and simulate Xbox inputs.

---

## Key Features

- **Basic Input Mapping**: Maps Meta Quest controller buttons, triggers, and joysticks to Xbox controller equivalents.
- **Real-time Conversion**: Converts inputs in real-time for smooth gameplay.
- **Cross-Platform Compatibility**: Works on Windows, macOS, and Linux.
- **Simple Configuration**: Easy-to-use configuration file to customize input mappings.
- **Plug and Play**: Automatically detects Meta Quest controllers when connected via USB or Bluetooth.

---

## Installation Guide

To install this project, follow these steps based on your operating system:

### 1. Windows
```bash
git clone https://github.com/yourusername/meta-quest-to-xbox.git
cd meta-quest-to-xbox
mkdir build
cd build
cmake ..
cmake --build .
