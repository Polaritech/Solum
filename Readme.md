# Solum - A Simple Rendering Engine

Solum is a simple rendering engine written in C++ designed to allow runtime swapping of rendering drivers (i.e., OpenGL → DirectX 11 → Vulkan). It utilizes modern C++ features and compiles with tools later than G++ 6 and MSVC 2017.

Solum comes with some utility functionality to make using the renderers easier:
 * Cross platform windowing functions

### Building

On Windows building is performed using Visual Studio. Simply load the solution from `Scripts/VS2017.sln` into Visual Studio and build it normally.

On Linux building is performed using G++ and Make. Simply open a terminal, go to the `Build` directory, and run the make command as `make -f ../Scripts/Makefile`. The extended make command is used to build the source outside of the source tree.

### Using

On both Windows and Linux Solum is built as a library (static or shared can be configured). To use Solum, your program simply has to add Solum's include directory and link to the library.

Once the code is linked, you can begin programming. To draw a triangle to the screen using OpenGL, simply compile the following code:

```cpp
int main(int argc, char **argv) {
	// Todo: Add actual code here!
}
```