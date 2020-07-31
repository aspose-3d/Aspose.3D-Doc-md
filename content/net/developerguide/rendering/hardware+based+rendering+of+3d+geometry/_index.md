---
title : "Hardware Based Rendering of 3D Geometry" 
description : "" 
weight : 12056 
toc : false
type: docs
url: /net/developerguide/rendering/hardware+based+rendering+of+3d+geometry/
---

# Aspose.3D for .NET : Hardware Based Rendering of 3D Geometry


Using [Aspose.3D for .NET](http://www.aspose.com/3d-component-suite.aspx) API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. In this article, we focus on hardware-based rendering using [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489(v=vs.85).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327(v=vs.85).aspx) and [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{< panel title="Contents Summary" style="primary" >}}
*   1 [Create Hardware and Render a 3D Geometry](#create-hardware-and-render-a-3d-geometry)
    *   1.1 [Programming Sample for Shader](#programming-sample-for-shader)
    *   1.2 [Programming Sample for the Buffer and Render State](#programming-sample-for-the-buffer-and-render-state)
{{< /panel >}}
 

 

## Create Hardware and Render a 3D Geometry

To render a 3D geometry, a shader, buffers and render state are required. None of them can work without each other.

*   **Buffers** - Triangle lists are individual triangles specified in an array that is sometimes referred to as a buffer. In a triangle list, each triangle is individually specified. Points of a triangle can be shared by using indices to reduce the amount of data that must be passed to the graphics hardware.
*   **Shaders** - It defines how to transform the triangles from world space into screen space and calculate the final pixel color in GPU side
*   **Render States** - It provides parameters for the GPU to rasterize the triangles into pixels.

We have prepared a demo project. Please refer to [this download URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

The OpenGL Shading Language (GLSL) is the standard high level shading language for the OpenGL graphics API. The **InitRenderer** method in **AssetBrowser/Controls/RenderView.cs** file under the demo application (name:AssetBrowser) demonstrates the simple use of GLSL using Aspose.3D API. There are three shader types commonly used: Vertex Shaders, Fragment Shaders and Geometry Shaders.

[GLSLSource](http://www.aspose.com/api/net/3d/aspose.threed.render/glslsource) class tells the renderer, the source code is for OpenGL shading language, it can be compiled to [ShaderProgram](http://www.aspose.com/api/net/3d/aspose.threed.render/shaderprogram) class. The [ShaderVariable](http://www.aspose.com/api/net/3d/aspose.threed.render/shadervariable) class defines the variables used in the shader. The [VariableSemantic](http://www.aspose.com/api/net/3d/aspose.threed.render/variablesemantic) class is used to identify the shader variable's semantic, Aspose.3D renderer will automatically prepare shader variable values depends on the semantics.

### Programming Sample for Shader

This code example initializes renderer and Shader for the grid. You can download complete working project of this example from [here](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

### Programming Sample for the Buffer and Render State

This code example initializes the buffer and render state for the grid.

