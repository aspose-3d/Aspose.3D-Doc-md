---
title: Hårdvarubaserad hyllning av 3D Geometria
type: docs
weight: 30
url: /sv/python-net/hardware-based-rendering-of-3d-geometry/
description: Genom att använda Aspose.3D for Python via .NET API, kan utvecklare programmera GPU (grafikbehandlingsenheten) och ställa in grafik hårdvara för att visa 3D geometri istället för den fasta funktionspipelinen
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, kan utvecklare programmera GPU (grafikbehandlingsenheten) och ställa in grafik hårdvara för att visa 3D geometri istället för den fasta funktionspipelinen I den här artikeln fokuserar vi på hårdvarabaserad rendering med [OpenGL 4. 0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). aspx) och [Vulkan Ordförande](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Skapa hårdvara och renter a 3D Geometria**
För att visa en 3D- geometri krävs en skuggar, buffertar och renderingstillstånd. Ingen av dem kan arbeta utan varandra.

- **Buffertar**- Triangellistor är enskilda trianglar som anges i ett matris som ibland kallas buffert. I en triangellista, varje triangel anges individuellt. Punkter i en triangel kan delas genom att använda index för att minska mängden data som måste skickas till grafik maskinvaran.
- **Skuggar**- Det definierar hur man omvandlar trianglar från världsutrymme till skärm och beräknar den slutliga pixelfärgen i GPU sidan
- **Render stater**- Det ger parametrar för GPU att rasterisera trianglarna i pixlar.

{{% alert color="primary" %}}

Vi har förberett ett demoprojekt. Se [Den här webbadressen för nedladdning](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

OpenGL-skuggande språk (GLSL) är det standardiserade språket på hög nivå för OpenGL-grafiken API. Det finns tre skugga typer som vanligen används: Vertex Shaders, Fragment Shaders och Geometri Shaders.

[`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) klassen talar om för renderare, källkoden är för OpenGL- skuggningsspråk, den kan kompileras till [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) klass. [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable)-klassen definierar de variabler som används i skuggarn. Klassen `VariableSemantic` används för att identifiera skuggarvariablens semantiska, Aspose. 3D renderare förbereder automatiskt skuggarvariabelvärden beror på semantiken.
###  **Programmeringsprov för skuggar**
Det här kodexemplet initierar renderare och Shader för rutnätet. Du kan ladda ner komplett arbetsprojekt med detta exempel från [Här](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
###  **Programmeringsprov för buffert- och rendertillstånden**
Det här kodexemplet initierar bufferten och renderingstillståndet för rutnätet.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
