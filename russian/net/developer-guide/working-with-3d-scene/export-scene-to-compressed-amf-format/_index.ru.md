---
title: Экспорт сцены в сжатый формат AMF
type: docs
weight: 30
url: /ru/net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET предлагает класс AmfSaveOptions, который позволяет вам установить значение bool для сжатия в соответствии с вашими требованиями. По умолчанию значение имеет значение true.
---
##  **Экспорт сцены в сжатый формат AMF**
Aspose.3D for .NET предлагает класс `AmfSaveOptions`, который позволяет вам установить значение bool для сжатия в соответствии с вашими требованиями. По умолчанию значение имеет значение true. Следующий фрагмент кода показывает полную функциональность для создания сжатого файла формата AMF:

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
