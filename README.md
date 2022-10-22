# OpenGL

## 1. Welcome to OpenGL

OpenGL is:
- Just a specification. (similar to c/c++ language specification)
- Cross platform (not optimal, native is usualy more powerful/better)
- Easier to learn (Vulcan is an alternative but newer)

OpenGL is not:
- open source (GPU manufacturer's drivers include OpenGL implementation)
- a library (no code to include, compile, link, etc.)

OpenGL history:
- "Legacy" OpenGL (v1) started in 90's (think limited preset options)
- "Modern" OpenGL (v2-v4) has more low-level control of GPU

## 2. Setting up OpenGL and Creating a Window

- [Setup Tutorial (Mac)](https://www.youtube.com/watch?v=7-dL6a5_B3I&t=3s)

"Windowing" is very Platform specific (OS level thing)
- Windows: win32 API
- Linux: X11
- Mac: ?

Cross-Platform options for windowing:
- GLFW 
    - lightweight
    - used in this example
- SDL 
    - full framework
- wxWidgets
    - see KiCAD as example

## 3. Modern OpenGL
- GLFW: Window, run loop, process input, etc.
- GLAD or GLEW: Manages function pointers for "Modern" OpenGL
    - Extracts available functions from your GPU
- OpenGL: Graphics API. Access GPU
    - Alternatives to OpenGL: Direct 3D (Windows), Vulcan (Cross Platform), Metal (MacOS)
- Two steps
    - Create Vertex Buffer: Array of data that lives on the GPU
    - Shader: Code that runs on GPU for how to use data
- OpenGL is a state machine. Standard workflow:
    - Select vertex buffer (Give GPU data)
    - Select Shader (Program to execute)
    - Draw Object (Actual Execution)

## 4. Vertex Buffers and Drawing a Triangle

## 5. Vertex Attributes and Layouts

## 6. How Shaders Work

Two primary types: Vertex, Fragment (pixel) shaders. But many other types: Geometry, Compute, etc.

(Simplified) Order
1. Draw Call
2. Vertex Shader (Called for each vertex. Example) Triangle has three calls)
    - Can pass data from Vertex Shader to Fragment Shader
3. Fragment Shader (Run once for each pixel that needs to be drawn (i.e. thousands). Mainly color)
    - Example is lighting. Env, texture, lighting, material, camera, etc come together to determine color
4. Result on screen

- 80-90% in these two shaders. 
- Really good graphics can be 1000s of lines of code in a shader.
- Game engines generate shaders on the fly based on settings, context, etc.

## 7. Writing a Shader in OpenGL


Notes:
- I installed GLFW via `brew install glfw` but instead of using the dynamic library, I'm using a static library built from CMake and the glfw source code. The headerfile is from the brew install.



## Build
`Cmd+Shift+B`: Execute default build task in VSCode

## Run
`Cntr+Alt+T`: Run executable

or

```
./build/app
```

## Resources


- [GLFW Docs](https://www.glfw.org/documentation.html)
- [The Cherno](https://www.youtube.com/watch?v=OR4fNpBjmq8&list=PLlrATfBNZ98foTJPJ_Ev03o2oq3-GGOS2&index=2)
- [OpenGL API](https://docs.GL)
