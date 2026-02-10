---
title: Sahneyi sıkıştırılmış AMF formatına aktar
type: docs
weight: 30
url: /tr/net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET, gereksinimlerinize göre sıkıştırma için bool değerini ayarlamanızı sağlayan amfsaveoptions sınıfı sunar. Varsayılan olarak değer doğrudur.
---
##  **Sahneyi sıkıştırılmış AMF formatına aktar**
Aspose.3D for .NET, gereksinimlerinize göre sıkıştırma için bool değerini ayarlamanızı sağlayan `AmfSaveOptions` sınıfı sunar. Varsayılan olarak değer doğrudur. Kod parçacığı aşağıdaki sıkıştırılmış AMF format dosyası oluşturmak için tam işlevselliği gösterir:

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
