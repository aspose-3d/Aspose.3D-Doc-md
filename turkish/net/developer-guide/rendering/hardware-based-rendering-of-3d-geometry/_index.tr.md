---
title: Donanım tabanlı 3D geometrisinin oluşturulması
type: docs
weight: 30
url: /tr/net/hardware-based-rendering-of-3d-geometry/
description: Using Aspose.3D for .NET API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. 
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, developers can program the GPU (graphics processing unit) and setup the graphics hardware for rendering 3D geometry instead of the fixed function pipeline. In this article, we focus on hardware-based rendering using [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) and [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Donanım oluşturun ve 3D geometrisini oluşturun**
3D geometrisini oluşturmak için gölgelendirici, tampon ve render durumu gereklidir. Hiçbiri birbirleri olmadan çalışamaz.

- **Buffers**-Triangle listeleri, bazen tampon olarak adlandırılan bir dizide belirtilen bireysel üçgenlerdir. In bir üçgen listesi, her üçgen ayrı ayrı belirtilir. Bir üçgenin kısıtlamaları, grafik donanımına geçmesi gereken veri miktarını azaltmak için endeksleri kullanarak paylaşılabilir.
- **Shaders**-It, üçgenleri dünya alanından ekran alanına nasıl dönüştüreceğini ve son piksel rengini GPside side olarak hesaplamayı tanımlar.
- **Render tates tates**-It, üçgenleri piksele dönüştürmek için GPU için parametreler sağlar.

{{% alert color="primary" %}}

We have prepared a demo project. Please refer to [this download URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

The OpenGL Shading Language (GLSL) is the standard high level shading language for the OpenGL graphics API. The `InitRenderer` method in `AssetBrowser/Controls/RenderView.cs` file under the demo application (name:AssetBrowser) demonstrates the simple use of GLSL using Aspose.3D API. There are three shader types commonly used: Vertex Shaders, Fragment Shaders and Geometry Shaders.

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) sınıfı kiracıya söyler, kaynak kodu opengl gölgeleme dili içindir, [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) sınıfına derlenebilir. [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) sınıfı gölgelendiricide kullanılan değişkenleri tanımlar. `VariableSemantic` sınıfı, gölgelendirici değişkeninin semantik, Aspose.3D renderer otomatik olarak gölgelendirici değişken değerlerini semantiklere göre hazırlayacaktır.
###  **Srogramming SShader için yeterli**
Bu kod örneği, ızgara için renderer ve gölgelendirici başlatır. Bu örneğin tam çalışma projesini [Burada](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering) 'dan indirebilirsiniz.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Controls-RenderView-RenderView.cs" >}}
###  **Brogramming ffer Buffer ve Render State için yeterli**
Tkod örneği tamponu başlatır ve ızgara için durum oluşturur.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Grid-ManualEntity.cs" >}}
