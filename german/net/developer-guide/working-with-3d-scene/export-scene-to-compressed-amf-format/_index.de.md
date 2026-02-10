---
title: Szene in komprimiertes AMF-Format exportieren
type: docs
weight: 30
url: /de/net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET bietet die AmfSaveOptions-Klasse, mit der Sie den Bool-Wert für die Kom primi erung gemäß Ihren Anforderungen festlegen können. Standard mäßig ist der Wert auf true gesetzt.
---
##  **Szene in komprimiertes AMF-Format exportieren**
Aspose.3D for .NET bietet die `AmfSaveOptions`-Klasse, mit der Sie den Bool-Wert für die Kom primi erung gemäß Ihren Anforderungen festlegen können. Standard mäßig ist der Wert auf true gesetzt. Das folgende Code-Snippet zeigt die vollständige Funktional ität zum Generieren einer komprimierten AMF-Format datei:

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
