---
title: Hardware Based 07en07of 3D eoeometry
type: docs
weight: 30
url: /tr/net/hardware-based-rendering-of-3d-geometry/
description: 07sing Aspose.3D for .NET API, geliştiriciler Ggraphics U (grafik işlem birimi) programlayabilir ve sabit fonksiyon boru hattı yerine 3D geometrisini oluşturmak için grafik donanımını kurabilirler.
---
{{% alert color="primary" %}}

Using[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API, geliştiriciler GPU (grafik işlem birimi) programlayabilir ve sabit fonksiyon boru hattı yerine 3D geometrisini oluşturmak için grafik donanımını kurabilirler. Bu makaleyi kullanarak, donanım tabanlı işleme odaklanıyoruz[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) ve[Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
## **07reate Hardware ve Render a 3D eoeometry**
To bir 3D geometrisi, bir gölgelendirici, tamponlar ve render durumu gereklidir. Bunlardan biri birbirleri olmadan çalışabilir.

- **Buffers**-Triangle listeleri, bazen tampon olarak adlandırılan bir dizide belirtilen bireysel üçgenlerdir. In bir üçgen listesi, her üçgen ayrı ayrı belirtilir. Bir üçgenin kısıtlamaları, grafik donanımına geçmesi gereken veri miktarını azaltmak için endeksleri kullanarak paylaşılabilir.
- **Shaders**-It, üçgenleri dünya alanından ekran alanına nasıl dönüştüreceğini ve son piksel rengini GPside side olarak hesaplamayı tanımlar.
- **Render tates tates**-It, üçgenleri piksele dönüştürmek için GPU için parametreler sağlar.

{{% alert color="primary" %}}

We bir demo projesi hazırladı. Please bakın[Bu indirme UL L](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

The OpenGL Shading guage anguage (GLL L) OpenGL grafik API için standart yüksek seviye gölgeleme dilidir. 076481 481 dosyasında demo he `InitRenderer` yöntemi demo uygulaması altında (ad: Asset. rowser), 076481 481 API kullanarak GLL L 'in basit kullanımını gösterir. Tburada yaygın olarak kullanılan üç gölgelendirici türü vardır: Vertex Shaders, gment ragment ders haders ve Geometry Shaders.

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) sınıfı kiracıya söyler, kaynak kodu OpenGL gölgeleme dili içindir, [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) sınıfına derlenebilir. The [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) sınıfı gölgelendiricide kullanılan değişkenleri tanımlar. Shader he 076. 481 sınıfı, gölgelendirici değişkeninin anlamlılığını tanımlamak için kullanılır, 076. 481 renderer otomatik olarak gölgelendirici değişken değerlerini semantiklere göre hazırlayacaktır.
### **Srogramming SShader için yeterli**
Kod örneği, ızgara için renderer ve Shader'ı başlatır. You bu örnek tam çalışma projesini indirebilir[Burada](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Controls-RenderView-RenderView.cs" >}}
### **Brogramming ffer Buffer ve Render State için yeterli**
Tkod örneği tamponu başlatır ve ızgara için durum oluşturur.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Grid-ManualEntity.cs" >}}
