---
title: Hardware basiertes Rendern der Geometrie 3D
type: docs
weight: 30
url: /de/net/hardware-based-rendering-of-3d-geometry/
description: Mithilfe der Aspose.3D for .NET APIkönnen Entwickler die GPU (Grafik verarbeitung einheit) programmieren und die Grafik hardware zum Rendern der Geometrie 3D anstelle der Pipeline mit fester Funktion einrichten.
---
{{% alert color="primary" %}}

Verwendung[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API können Entwickler die GPU (Grafik verarbeitung einheit) programmieren und die Grafik hardware zum Rendern der Geometrie 3D anstelle der Pipeline mit fester Funktion einrichten. In diesem Artikel konzentrieren wir uns auf hardware basiertes Rendering mit[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) und[Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
## **Hardware erstellen und eine Geometrie 3D ausstellen**
Um eine Geometrie 3D zu rendern, sind ein Shader, Puffer und ein Render zustand erforderlich. Keiner von ihnen kann ohne einander arbeiten.

- **Puffer**-Dreiecks listen sind einzelne Dreiecke, die in einem Array angegeben sind, das manchmal als Puffer bezeichnet wird. In einer Dreiecks liste wird jedes Dreieck einzeln angegeben. Punkte eines Dreiecks können mithilfe von Indizes gemeinsam genutzt werden, um die Datenmenge zu reduzieren, die an die Grafik hardware übergeben werden muss.
- **Shader**-Es definiert, wie man die Dreiecke aus dem Weltall in den Bildschirm raum transform iert und die endgültige Pixel farbe in der GPU-Seite berechnet
- **Render Staaten**-Es bietet Parameter für die GPU, um die Dreiecke in Pixel zu rastern.

{{% alert color="primary" %}}

Wir haben ein Demo-Projekt vorbereitet. Bitte beziehen Sie sich auf[Diese Download-URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

Die Schattierung sprache OpenGL (GLSL) ist die Standard-Schattierung sprache auf hohem Niveau für die OpenGL-Grafik API. Die Methode `InitRenderer` in der Datei `AssetBrowser/Controls/RenderView.cs` unter der Demo-Anwendung (Name: Asset Browser) demonstriert die einfache Verwendung von GLSL unter Verwendung von Aspose.3D API. Es werden häufig drei Shader-Typen verwendet: Vertex-Shader, Fragment-Shader und Geometry-Shader.

Die Klasse [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) teilt dem Renderer mit, dass der Quellcode für die Schattierung sprache OpenGL ist und in die Klasse [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) kompiliert werden kann. Die Klasse [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) definiert die im Shader verwendeten Variablen. Die Klasse `VariableSemantic` wird verwendet, um den semantischen Renderer der Shader-Variablen zu identifizieren. Aspose.3D Renderer bereitet automatisch Shader-Variablen werte vor, die von der Semantik abhängen.
### **Programmier probe für Shader**
Dieses Code beispiel initial isiert Renderer und Shader für das Raster. Sie können das komplette Arbeits projekt dieses Beispiels von herunter laden[Hier](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Controls-RenderView-RenderView.cs" >}}
### **Programmier probe für den Puffer-und Render zustand**
Dieses Code beispiel initial isiert den Puffer-und Render zustand für das Raster.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Grid-ManualEntity.cs" >}}
