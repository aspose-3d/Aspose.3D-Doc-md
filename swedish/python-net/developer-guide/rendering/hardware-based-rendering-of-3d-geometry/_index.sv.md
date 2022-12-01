---
title: Hårdvarubaserad rendering av 3D geometri.
type: docs
weight: 30
url: /sv/python-net/hardware-based-rendering-of-3d-geometry/
description: Med Aspose.3D för Python via .NET API kan utvecklare programmera GPU (grafikbearbetningsenheten) och ställa in grafik maskinvaran för rendering 3D geometri istället för den fasta funktionsrörledningen.
---
{{% alert color="primary" %}}

Användning[Aspose.3D för Python via .NET](https://products.aspose.com/3d/python-net/)API, utvecklare kan programmera GPU (grafikbearbetningsenheten) och ställa in grafik maskinvaran för rendering 3D geometri istället för den fasta funktionsrörledningen. I den här artikeln fokuserar vi på hårdvaru-baserad rendering med användningen[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx)[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) och aspx[Vulkan Ordförande](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
## **Skapa hårdvara och renter en 3D geometri.**
För att göra en 3D geometri krävs en skuggar, buffertar och render tillstånd. Ingen av dem kan arbeta utan varandra.

- **Buffertar**- Triangellistor är enskilda trianglar som anges i ett matris som ibland kallas buffert. I en triangellista, varje triangel anges individuellt. Punkter i en triangel kan delas genom att använda index för att minska mängden data som måste skickas till grafik maskinvaran.
- **Skuggar**- Det definierar hur man omvandlar trianglar från världsutrymme till skärm och beräknar den slutliga pixelfärgen i GPU sidan
- **Render stater**- Det ger parametrar för GPU att rasterisera trianglarna i pixlar.

{{% alert color="primary" %}}

Vi har förberett ett demoprojekt. Se med[Den här webbadressen för nedladdning](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

OpenGL Skugggspråk (GLSL) är standarden hög nivås språk för grafiken OpenGL API. Det finns tre skugga typer som vanligen används: Vertex Shaders, Fragment Shaders och Geometri Shaders.

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) klass berättar renderare, källkoden är för OpenGL språk, den kan sammanställas till [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) klass. Klassen [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) definierar de variabler som används i skuggarn. `VariableSemantic` klassen används för att identifiera skuggarvariablens semantiska, Aspose.3D render automatiskt förbereder variabla värden beror på semantik.
### **Programmeringsprov för skuggar**
Det här kodexemplet initierar renderare och Shader för rutnätet. Du kan ladda ner komplett arbetsprojekt av detta exempel från[Här](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
### **Programmeringsprov för buffert- och rendertillstånden**
Det här kodexemplet initierar bufferten och renderingstillståndet för rutnätet.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
