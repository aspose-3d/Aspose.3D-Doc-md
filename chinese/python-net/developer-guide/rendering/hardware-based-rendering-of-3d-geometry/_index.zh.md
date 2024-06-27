---
title: 3D 几何图形的基于硬件的呈现
type: docs
weight: 30
url: /zh/python-net/hardware-based-rendering-of-3d-geometry/
description: 使用 Aspose.3D for Python via .NET API，开发人员可以对GPU (图形处理单元) 进行编程，并设置图形硬件来渲染 3D 几何图形，而不是固定函数管道。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API，开发人员可以对GPU (图形处理单元) 进行编程，并设置图形硬件来渲染 3D 几何图形，而不是固定函数管道。在本文中，我们重点介绍使用 [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml) 、 [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx) 、 [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) 和 [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo) 的基于硬件的渲染。

{{% /alert %}}
##  **创建硬件并渲染 3D 几何体**
若要渲染 3D 几何体，需要着色器、缓冲区和渲染状态。他们都离不开彼此。

- **缓冲区**-三角形列表是在数组中指定的单个三角形，有时被称为缓冲区。在三角形列表中，每个三角形都是单独指定的。可以通过使用索引来减少必须传递给图形硬件的数据量来共享三角形的点。
- **着色器**-它定义了如何将三角形从世界空间转换为屏幕空间并计算GPU侧的最终像素颜色
- **渲染状态**-它为GPU提供了参数，以将三角形光栅化为像素。

{{% alert color="primary" %}}

我们准备了一个演示项目。请参阅 [这个下载网址](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering)。

{{% /alert %}}

OpenGL着色语言 (GLSL) 是OpenGL图形 API 的标准高级着色语言。有三种常用的着色器类型: 顶点着色器，片段着色器和几何着色器。

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) 类告诉渲染器，源代码是为OpenGL着色语言编写的，可以编译成 [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) 类。[`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) 类定义着色器中使用的变量。`VariableSemantic` 类用于标识着色器变量的语义 Aspose。3D 渲染器将根据语义自动准备着色器变量值。
###  **着色器的编程示例**
此代码示例初始化网格的渲染器和着色器。您可以从 [这里](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering) 下载此示例的完整工作项目。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
###  **缓冲区和渲染状态的编程示例**
此代码示例初始化网格的缓冲区和渲染状态。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
