# Solum ~ A Simple Rendering Engine

Solum is a simple rendering engine written in C++ designed to allow runtime swapping of rendering drivers (i.e., OpenGL → DirectX 11 → Vulkan). This allows developers to experiment with various rendering backends without much setup work on their part. It utilizes modern C++ features and compiles with tools later than G++ 6 and MSVC 2017.

Solum comes with some utility functionality to make using the renderers easier:
 * Cross platform windowing functions
 * A small linear algebra library
 * Basic user input functions

### Roadmap
Solum is in an early state, and requires quite a bit of work to get to a usable state. The project has the following tasks to do:
- [ ] Windowing
  - [ ] Windowing Interface
  - [ ] Win32 Window
  - [ ] XCB Window
- [ ] Rendering
  - [ ] Rendering Interface
    - [ ] Driver Interface
    - [ ] Adapter & Device Interfaces
    - [ ] Context Interface
    - [ ] Surface Interface
    - [ ] Shader Interface
  - [ ] DirectX 11 Rendering System
  - [ ] Vulkan Rendering System
  - [ ] OpenGL 3.3 Rendering System
- [ ] Math
  - [ ] Vectors
  - [ ] Matrices
- [ ] Input
  - [ ] Input Interface
    - [ ] Keyboard Interface
    - [ ] Mouse Interface
  - [ ] RawInput
  - [ ] XCB Input

Our current timeline for the beginning of 2017 is as follows:
- 01.24.2017 **Proposal Written**
- 01.27.2017 **Windowing Interface Designed**
- 02.06.2017 **Win32 Windowing Implementation**
- 02.20.2017 **Rendering Interface Designed**
- 02.27.2017 **DirectX 11 Initial Implementation**
- 03.06.2017 **Rendering & Window Interface Documentation**
- 03.13.2017 **Vulkan Initial Implementation**
- 03.20.2017 **Vector & Matrix Design**
- 03.27.2017 **Vector & Matrix Basic Functions**
- 04.03.2017 **Input Interface Designed & Documented**
- 04.10.2017 **Keyboard RawInput (Windows)**
- 04.17.2017 **XCB Windowing Implementation**
- 04.24.2017 **Keyboard XCB Input (Linux)**
- 05.01.2017 **Refine & Optimize Current Renderers**
- 05.08.2017 **Vulkan & DirectX 11 Specific Documentation**
- 05.15.2017 **OpenGL 3.3 Initial Implementation**
- 05.22.2017 **OpenGL 3.3 Optimization**
- 05.29.2017 **OpenGL 3.3 Documentation**

<!-- ### Building

On Windows building is performed using Visual Studio. Simply load the solution from `Scripts/VS2017.sln` into Visual Studio and build it normally.

On Linux building is performed using G++ and Make. Simply open a terminal, go to the `Build` directory, and run the make command as `make -f ../Scripts/Makefile`. The extended make command is used to build the source outside of the source tree.

### Using

On both Windows and Linux Solum is built as a library (static or shared can be configured). To use Solum, your program simply has to add Solum's include directory and link to the library.

Once the code is linked, you can begin programming. To draw a triangle to the screen using OpenGL, simply compile the following code:

```cpp
int main(int argc, char **argv) {
	// Todo: Add actual code here!
}
``` -->