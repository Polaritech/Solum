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

Our current timeline for the first half of 2017 is as follows:
- Milestone 0 **Setup**
  - 01.24.2017 **Proposal Written**
  - 01.27.2017 **Project Setup (Solution & Makefile)**
  - 01.31.2017 **Build & Usage Instructions**
- Milestone 1 **Windowing**
  - 02.07.2017 **Windowing Interface Designed**
  - 02.10.2017 **Win32 Windowing Implementation**
  - 02.14.2017 **XCB Windowing Implementation**
  - 02.17.2016 **Window Interface Documentation**
- Milestone 2 **Basic Rendering**
  - 02.21.2017 **Rendering Interface Designed**
  - 02.28.2017 **DirectX 11 Initial Implementation**
  - 03.07.2017 **OpenGL 3.3 Initial Implementation**
  - 03.17.2017 **Vulkan Initial Implementation**
  - 03.21.2017 **Rendering Interface Documentation**
  - 03.24.2017 **Renderer-Specific Documentation**
- Milestone 3 **Mathematics**
  - 03.28.2017 **Vector & Matrix Design**
  - 03.31.2017 **Vector & Matrix Basic Functions**
  - 04.04.2017 **Vector & Matrix Documentation**
- Milestone 4 **User Input**
  - 04.07.2017 **Input Interface Designed**
  - 04.11.2017 **Keyboard RawInput (Windows)**
  - 04.14.2017 **Keyboard XCB Input (Linux)**
  - 04.18.2017 **Input Interface Documentation**
- Milestone 5 **Rendering Optimizations**
  - 04.25.2017 **DirectX 11 Optimization**
  - 05.16.2017 **OpenGL 3.3 Optimization**
  - 06.06.2017 **Vulkan Optimization**
  - 06.20.2017 **Rendering Optimization Documentation**