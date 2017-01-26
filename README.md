# Solum ~ A Simple Rendering Engine
Solum is a simple rendering engine written in C++ designed to allow runtime swapping of rendering drivers (i.e., OpenGL → DirectX 11 → Vulkan). This allows developers to experiment with various rendering backends without much setup work on their part. It utilizes modern C++ features and compiles with tools later than G++ 6 and MSVC 2017.

Solum comes with some utility interfaces to make using the rendering backends easier:
- A Windowing Interface.
- A Mathematics Interface.
- A User Input Interface.

## Getting Started
### Prerequisites
#### Windows
- Visual Studio 2017

#### Linux
- GNU Make 
- G++ 6

### Building
#### Windows
- Open the solution file `Scripts/VS2017/Solum.sln` in Visual Studio 2017.
- Run the build command.

#### Linux
- Open a terminal in the `Build` directory.
- Run the command `make -f ../Scripts/Makefile`

### Using the Library
#### Windows
- Import the import library found at `Build/<Arch>/<Config>/Output/Solum.lib`.
- Include the headers in `Include`.
- Place the dynamic library found at `Build/<Arch>/<Config>/Output/Solum.dll` in your project's build directory.

#### Linux
- Include the headers in `Include`.
- Add the link flags `-L Build/<Arch>/<Config>/Output -lsolum`.
- Add `/Build/<Arch>/<Config>/Output` to your `LD_LIBRARY_PATH` variable.

## Contributing
To contribute so Solum, take a look at the [contributing guidelines](http://git.polaritech.com/Polaritech/Solum/blob/master/CONTRIBUTING.md), as well as the [style guidelines](http://git.polaritech.com/Polaritech/Solum/blob/master/Documentation/StyleGuide.md).