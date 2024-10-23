# Meta Quest to Xbox Controller Input Converter

## Project Overview

The **Meta Quest to Xbox Controller Input Converter** is a C++ application designed to convert the input signals from Meta Quest 2 and Meta Quest 3 controllers into Xbox controller inputs. This allows you to use your Meta Quest controllers for games and applications that support Xbox controllers on Windows, macOS, and Linux. This project is aimed at junior developers who are interested in input mapping and game development.

## Key Features

- **Controller Input Mapping**: Maps Meta Quest controller inputs to Xbox controller inputs seamlessly.
- **Cross-Platform Support**: Works on Windows, macOS, and Linux.
- **Simple Installation**: Easy to set up using CMake.
- **Custom Input Profiles**: Create and use custom profiles for different games.
- **Optional Scripting**: Integrate scripts for advanced functionality and automation.

## Installation Guide

### Prerequisites

Make sure you have the following installed:

- CMake
- A C++ compiler (e.g., g++, clang++, or MSVC)

### Installation Steps

#### Windows

1. Download the [CMake](https://cmake.org/download/) installer and install it.
2. Open a command prompt and run the following commands:

   ```bash
   git clone https://github.com/yourusername/meta-quest-to-xbox-controller.git
   cd meta-quest-to-xbox-controller
   mkdir build
   cd build
   cmake ..
   cmake --build .
   ```

#### macOS

1. Install [Homebrew](https://brew.sh/) if you haven't already, then install CMake:

   ```bash
   brew install cmake
   ```

2. Open a terminal and run the following commands:

   ```bash
   git clone https://github.com/yourusername/meta-quest-to-xbox-controller.git
   cd meta-quest-to-xbox-controller
   mkdir build
   cd build
   cmake ..
   cmake --build .
   ```

#### Linux

1. Open a terminal and install CMake if it's not already installed:

   ```bash
   sudo apt-get install cmake
   ```

2. Run the following commands:

   ```bash
   git clone https://github.com/yourusername/meta-quest-to-xbox-controller.git
   cd meta-quest-to-xbox-controller
   mkdir build
   cd build
   cmake ..
   cmake --build .
   ```

## How It Works

The converter uses input mapping techniques to read data from Meta Quest controllers and simulate Xbox controller inputs. The program listens for input events from the Meta Quest controllers and translates them into corresponding Xbox controller signals using a predefined mapping table.

### Code Snippet

Here's a simple example of how the program captures Meta Quest controller inputs and maps them to Xbox controller inputs:

```cpp
#include <iostream>
#include <OpenXR/OpenXR.h> // OpenXR library
#include <vJoyInterface.h> // vJoy library for Xbox inputs

void mapInput(XR_INPUT_ACTION action) {
    switch (action) {
        case XR_INPUT_ACTION_BUTTON_A:
            vJoySetButton(1); // Map to Xbox A button
            break;
        case XR_INPUT_ACTION_BUTTON_B:
            vJoySetButton(2); // Map to Xbox B button
            break;
        // Add additional mappings as needed
    }
}
```

## Usage Instructions

1. Connect your Meta Quest controllers to your computer via USB or Bluetooth.
2. Run the program by navigating to the build directory and executing the binary:

   ```bash
   ./meta-quest-to-xbox-controller
   ```

3. The program will start mapping the inputs. You can check the console for any errors or messages.

## Troubleshooting

- **Controller Not Recognized**: Ensure that the controllers are properly connected and recognized by your operating system.
- **Input Lag**: Check for any background applications that may interfere with input processing.
- **Compilation Errors**: Ensure that you have installed all prerequisites and are using the correct compiler version.

## Advanced Features

- **Custom Input Profiles**: You can create custom input profiles by editing the configuration file located in the `config` directory.
- **Optional Scripting**: Use scripts to automate certain actions or to create complex input mappings.

## Technologies Used

- **OpenXR**: A cross-platform open standard for VR and AR applications, enabling access to VR hardware.
- **vJoy**: A virtual joystick driver that allows software applications to emulate joystick inputs.

## Contributing

We welcome contributions! If you'd like to contribute, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to reach out if you have any questions or need further assistance!
```

### Notes:
- Adjust the GitHub URL in the installation steps as needed.
- Ensure to include any specific libraries or additional setup steps that might be required for your project.
- Replace the placeholder action mappings in the code snippet with actual mappings relevant to your implementation.
