# A Vulkan Rasterizer

This C++ project is to build a modern rasterization pipeline around the Vulkan graphics API. 

![vulkan_pipeline_block_diagram](https://user-images.githubusercontent.com/25319668/221376812-bfd1e65e-19df-440b-b30f-47f6c5b1b728.png)


In deferred lighting model, we render objects to G-Buffer first and then render lights reading from G-Buffer. In forward mode, lights and objects are coupled together.

***NOTE:*** Lighting architecture choice (Forward/Deferred/Tile Based Forward/Tile Based Deferred) is how we orchestrate Vulkan API not a built-in part of Vulkan or any other Graphics APIs.

https://user-images.githubusercontent.com/25319668/218864367-92a76afc-626b-4aa5-8d90-f4a6bf27d9d2.mp4

## About

Modern Vulkan Graphics API is important in many ways.
This project uses Vulkan to build a rasterization pipeline on Apple Silicon M1/2 chip.

Rasterizer incudes: projective camera, shader loading and parsing, Vulkan pipeline components: Device, Swap Chain, Command Buffer, Descriptor, Push Constant, loading obj models, multi-point Lighting, alpha blending and more.
Meanwhile, you can move the camera around using keyboard keys.
## Requirements

C++ Lib:
* GLM
* GLFW

Vulkan SDK:
* https://vulkan.lunarg.com/sdk/home

## Build on MacOS

C++17 is needed to compile the project.
```
./macBuild
```
## Run on MacOS
```
cd build
./Vulkan-Rasterizer
```

## Keyboard Controls

* W/A/S/D/E/Q to change the camera positions.

* Arrow key up/left/right/down to rotate the camera.
