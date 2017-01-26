# Solum ~ A Simple Rendering Engine
Solum is a simple rendering engine written in C++ designed to allow runtime swapping of rendering drivers (i.e., OpenGL → DirectX 11 → Vulkan). This allows developers to experiment with various rendering backends without much setup work on their part. It utilizes modern C++ features and compiles with tools later than G++ 6 and MSVC 2017.

Solum comes with some utility interfaces to make using the rendering backends easier:
- A Windowing Interface.
- A Mathematics Interface.
- A User Input Interface.

## Goals
### Implement a Windowing Interface
To allow cross platform rendering, a windowing interface is essential. It allows applications to output to the screen, as well as recieve messages from the operating system (such as input messages).
#### Features
- [ ] Windows using the Win32 API.
- [ ] X11 on Linux using either XCB and/or Xlib.

### Design a Rendering Interface
As the goal of this project is to experiment with rendering using multiple backends, a consistent rendering interface is extremely important. Features that are specific to a single backend will be exported as rendering extensions.
#### Features
- [ ] DirectX
  - [ ] Version 11
- [ ] OpenGL
  - [ ] Version 3.3 Core
- [ ] Vulkan

### Design a Mathematics Interface
To assist with rendering, a linear algebra library is necessary. Having static objects is not as interesting as being able to transform and scale objects.
#### Features
- [ ] Vector Operations
- [ ] Matrix Operations
- [ ] Optimized Trigonometric Functions

### Design a User Input Interface
Receiving input from the user is a vital part of almost all applications. Controlling a scene using the keyboard or mouse will not only help with debugging but allow more control within an application.
#### Features
- [ ] Keyboard
- [ ] Mouse

### Stretch - Rendering Optimizations
Adding more support for certain rendering operations will allow developers to begin testing more advanced rendering techniques.

## Roadmap
Solum is in an early state, and requires quite a bit of work to get to a usable state. Out current timeline for the first half of 2017 is as follows:
Our current timeline for the first half of 2017 is as follows:
- Milestone 0 **Setup**
  - 01.24.2017 **Proposal Written**
  - 01.27.2017 **Visual Studio Solution Created**
  - 01.31.2017 **Makefile Created**
  - 01.31.2017 **Build & Usage Instructions Written**
- Milestone 1 **Windowing**
  - 02.07.2017 **Windowing Interface Designed**
  - 02.10.2017 **Win32 Windowing Implemented**
  - 02.14.2017 **XCB Windowing Implemented**
  - 02.14.2017 **Xlib Windowing Implemented**
  - 02.17.2016 **Window Interface Documented**
- Milestone 2 **Basic Rendering**
  - 02.21.2017 **Rendering Interface Designed**
  - 02.28.2017 **DirectX 11 Initial Implemented**
  - 03.07.2017 **OpenGL 3.3 Initial Implemented**
  - 03.17.2017 **Vulkan Initial Implemented**
  - 03.21.2017 **Rendering Interface Documented**
  - 03.24.2017 **Renderer-Specific Documented**
- Milestone 3 **Mathematics**
  - 03.28.2017 **Mathematics Interface Designed**
  - 03.31.2017 **Vector Operations Implemented**
  - 03.31.2017 **Matrix Operations Implemented**
  - 04.04.2017 **Optimized Trigonometric Functions Implemented**
  - 04.04.2017 **Mathematics Interface Designed**
- Milestone 4 **User Input**
  - 04.07.2017 **Input Interface Designed**
  - 04.11.2017 **Keyboard (RawInput) Implemented**
  - 04.11.2017 **Mouse (RawInut) Implemented**
  - 04.14.2017 **Keyboard (XCB) Implemented**
  - 04.14.2017 **Mouse (XCB) Implemented**
  - 04.14.2017 **Keyboard (Xlib) Implemented**
  - 04.14.2017 **Mouse (Xlib) Implemented**
  - 04.18.2017 **Input Interface Documented**

## Administration
Our team currently consists of [Adrian J. Collado](https://github.com/AdrianCollado) and [Nicholas Fogg](https://github.com/Exxion).

Adrian has the following responsibilities:
- Project & Team Management
- Engine Development

Nick has the following responsibilities:
- Engine Development

Developers will work on individual [issues](http://git.polaritech.com/Solum/Solum/issues), working towards the completion of a [milestone](http://git.polaritech.com/Solum/Solum/milestones). Issues will be managed using [issue boards](http://git.polaritech.com/Solum/Solum/boards).

Each set of commits that are used to complete a particular issue will follow the guidelines found in the [contribution guidelines](http://git.polaritech.com/Solum/Solum/blob/master/CONTRIBUTING.md). Code will be formatted according to the [style guidelines](http://git.polaritech.com/Solum/Solum/blob/master/Documentation/StyleGuide.md).

