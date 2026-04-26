## Overview

This project is a simple GUI menu system built using C and compiled on various platforms. The core functionality includes creating a window, handling user input, rendering rectangles, and displaying text. It uses custom header files for organizing code and multiple makefiles for cross-platform compilation.

## Features

- **Window Creation**: Creates a window with specified width and height.
- **Event Handling**: Handles mouse click events to select menu items.
- **Rendering**: Renders rectangles on the screen at specified positions and sizes.
- **Text Rendering**: Displays text at specified positions.
- **Cross-Platform Compilation**: Supports Linux, Windows, Wine (for Windows under Linux), and WebAssembly (via Emscripten).

## Project Structure

```
Gui_MenuSystem/
├── build/              # .exe files produced by Main.c
├── src/                # Source code directory
│   ├── Main.c          # Entry point of the application
│   └── *.h             # Header files for the source code
└── Makefile.linux      # Linux Build configuration
└── Makefile.windows    # Windows Build configuration
└── Makefile.wine       # Wine Build configuration
└── Makefile.web        # Emscripten Build configuration
└── README.md           # This file
```

### Prerequisites

- **C/C++ Compiler and Debugger**: GCC for Linux, Clang for cross-compilation, mingw64-gcc for Windows under Wine.
- **Make utility**: For building the project.
- **Standard development tools**: Required to compile C code.
- **Libraries**:
  - X11 for Linux window management.
  - png/jpeg libraries for image handling.
  - Additional libraries depending on the target platform (e.g., user32, gdi32 for Windows).

## Build & Run

### Building

To build the project for a specific operating system:

- **Linux**:
  ```sh
  make -f Makefile.linux all
  ```

- **Windows**:
  ```sh
  make -f Makefile.windows all
  ```

- **Wine (for Windows under Linux)**:
  ```sh
  make -f Makefile.wine all
  ```

- **WebAssembly (via Emscripten)**:
  ```sh
  make -f Makefile.web all
  ```

### Running

To run the compiled executable:

- **Linux**:
  ```sh
  make -f Makefile.linux exe
  ```

- **Windows**:
  ```sh
  make -f Makefile.windows exe
  ```

- **Wine (for Windows under Linux)**:
  ```sh
  make -f Makefile.wine exe
  ```

- **WebAssembly (via Emscripten)**:
  Open the generated `index.html` file in a web browser.

### Clean and Rebuild

To clean the build artifacts:

```sh
make -f Makefile.(os) clean
```

Then rebuild:

```sh
make -f Makefile.(os) all
```

These instructions should provide a comprehensive guide to building and running the project on various platforms.