---
title: Export Scene to Compressed AMF Format
type: docs
weight: 30
url: /net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET offers AmfSaveOptions class which allows you to set bool value for compression as per your requirements. By default the value is set to true. 
---

## **Export Scene to Compressed AMF Format**
Aspose.3D for .NET offers `AmfSaveOptions` class which allows you to set bool value for compression as per your requirements. By default the value is set to true. Following code snippet shows complete functionality to generate compressed AMF format file:

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
