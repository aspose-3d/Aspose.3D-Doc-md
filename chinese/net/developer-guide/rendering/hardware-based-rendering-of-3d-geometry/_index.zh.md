---
title: 基于硬件的3D几何图形渲染
type: docs
weight: 30
url: /zh/net/hardware-based-rendering-of-3d-geometry/
description: 使用Aspose.3D for .NET API，开发人员可以对GPU (图形处理单元) 进行编程，并设置用于渲染3D几何图形而不是固定功能流水线的图形硬件。
---
{{% alert color="primary" %}}

使用[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API，开发人员可以对GPU (图形处理单元) 进行编程，并设置用于渲染3D几何图形而不是固定功能流水线的图形硬件。在本文中，我们将重点放在基于硬件的渲染上，使用[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\)。aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\)。aspx) 和[Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)。

{{% /alert %}}
## **创建硬件并渲染3D几何图形**
要渲染3D几何图形，需要着色器、缓冲区和渲染状态。没有彼此，他们都无法工作。

- **缓冲区**-三角形列表是在数组中指定的单个三角形，有时被称为缓冲区。在三角形列表中，每个三角形都是单独指定的。可以通过使用索引来减少必须传递给图形硬件的数据量来共享三角形的点。
- **着色器**-它定义了如何将三角形从世界空间转换为屏幕空间并计算GPU侧的最终像素颜色
- **渲染状态**-它为GPU提供了参数，以将三角形光栅化为像素。

{{% alert color="primary" %}}

我们准备了一个演示项目。请参考[这个下载网址](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering)。

{{% /alert %}}

OpenGL着色语言 (GLSL) 是OpenGL图形API的标准高级着色语言。演示应用程序 (名称: AssetBrowser) 下`AssetBrowser/Controls/RenderView.cs`文件中的`InitRenderer`方法演示了使用Aspose.3D API简单使用GLSL。常用的着色器类型有三种: 顶点着色器、片段着色器和几何着色器。

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource)类告诉渲染器，源代码是针对OpenGL着色语言的，它可以编译为[`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram)类。[`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable)类定义着色器中使用的变量。`VariableSemantic`类用于标识着色器变量的语义，Aspose.3D渲染器将根据语义自动准备着色器变量值。
### **着色器的编程示例**
此代码示例初始化网格的渲染器和着色器。您可以从以下位置下载本示例的完整工作项目[这里](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering)。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Controls-RenderView-RenderView.cs" >}}
### **缓冲区和渲染状态的编程示例**
此代码示例初始化网格的缓冲区和渲染状态。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Grid-ManualEntity.cs" >}}
