---
title: Exportar escena a formato AMF comprimido
type: docs
weight: 30
url: /es/net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET ofrece la clase AmfSaveOptions que le permite establecer el valor bool para la compresión según sus requisitos. Por defecto, el valor es true.
---
##  **Exportar escena a formato AMF comprimido**
Aspose.3D for .NET ofrece la clase `AmfSaveOptions` que le permite establecer el valor de bool para la compresión según sus requisitos. Por defecto, el valor es true. El siguiente fragmento de código muestra la funcionalidad completa para generar un archivo de formato AMF comprimido:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load a scene
Scene scene = new Scene();
var box = new Box();
var tr = scene.RootNode.CreateChildNode(box).Transform;
tr.Scale = new Vector3(12, 12, 12);
tr.Translation = new Vector3(10, 0, 0);
tr = scene.RootNode.CreateChildNode(box).Transform;
// Scale transform
tr.Scale = new Vector3(5, 5, 5);
// Set Euler Angles
tr.EulerAngles = new Vector3(50, 10, 0);
scene.RootNode.CreateChildNode();
scene.RootNode.CreateChildNode().CreateChildNode(box);
scene.RootNode.CreateChildNode().CreateChildNode(box);
// Save compressed AMF file
scene.Save("Aspose.amf", new AmfSaveOptions() { EnableCompression = false });

{{< /highlight >}}
