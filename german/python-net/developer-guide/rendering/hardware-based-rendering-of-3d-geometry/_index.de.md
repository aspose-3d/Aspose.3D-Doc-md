---
title: Hardware basiertes Rendern von 3D Geometrie
type: docs
weight: 30
url: /de/python-net/hardware-based-rendering-of-3d-geometry/
description: Mit Aspose.3D for Python via .NET API können Entwickler die GPU (Grafik verarbeitung einheit) programmieren und die Grafik hardware zum Rendern von 3D Geometrie anstelle der Pipeline mit festen Funktionen einrichten.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API können Entwickler die GPU (Grafik verarbeitung einheit) programmieren und die Grafik hardware zum Rendern von 3D Geometrie anstelle der Pipeline mit festen Funktionen einrichten. In diesem Artikel konzentrieren wir uns auf hardware basiertes Rendering mit [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) und [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Hardware erstellen und eine 3D-Geometrie auszahlen**
Um eine 3D-Geometrie zu rendern, sind ein Shader, Puffer und ein Render zustand erforderlich. Keiner von ihnen kann ohne einander arbeiten.

- **Puffer**-Dreiecks listen sind einzelne Dreiecke, die in einem Array angegeben sind, das manchmal als Puffer bezeichnet wird. In einer Dreiecks liste wird jedes Dreieck einzeln angegeben. Punkte eines Dreiecks können mithilfe von Indizes gemeinsam genutzt werden, um die Datenmenge zu reduzieren, die an die Grafik hardware übergeben werden muss.
- **Shader**-Es definiert, wie man die Dreiecke aus dem Weltall in den Bildschirm raum transform iert und die endgültige Pixel farbe in der GPU-Seite berechnet
- **Render Staaten**-Es bietet Parameter für die GPU, um die Dreiecke in Pixel zu rastern.

{{% alert color="primary" %}}

Wir haben ein Demo-Projekt vorbereitet. Bitte beziehen Sie sich auf [Diese Download-URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

Die OpenGL Shading Language (GLSL) ist die Standard-Schattierung sprache auf hoher Ebene für die OpenGL-Grafik API. Es werden häufig drei Shader-Typen verwendet: Vertex-Shader, Fragment-Shader und Geometry-Shader.

Die [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource)-Klasse teilt dem Renderer mit, dass der Quellcode für die OpenGL-Shading-Sprache gilt und zu einer [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram)-Klasse kompiliert werden kann. Die [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable)-Klasse definiert die im Shader verwendeten Variablen. Die `VariableSemantic`-Klasse wird verwendet, um die semantische Aspose der Shader-Variable zu identifizieren. 3D Renderer bereitet automatisch Shader-Variablen werte vor, die von der Semantik abhängen.
###  **Programmier probe für Shader**
Dieses Code beispiel initial isiert Renderer und Shader für das Raster. Sie können das komplette Arbeits projekt dieses Beispiels von [Hier](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering) herunter laden.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
###  **Programmier probe für den Puffer-und Render zustand**
Dieses Code beispiel initial isiert den Puffer-und Render zustand für das Raster.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
