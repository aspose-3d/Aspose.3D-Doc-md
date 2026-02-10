---
title: Esporta la scena nel formato AMF compresso
type: docs
weight: 30
url: /it/net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET offre la classe AmfSaveOptions che ti consente di impostare il valore bool per la compressione secondo le tue esigenze. Per impostazione predefinita il valore è impostato su true.
---
##  **Esporta la scena nel formato AMF compresso**
Aspose.3D for .NET offre una classe `AmfSaveOptions` che ti consente di impostare il valore bool per la compressione secondo le tue esigenze. Per impostazione predefinita il valore è impostato su true. Il seguente frammento di codice mostra la funzionalità completa per generare file in formato AMF compresso:

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
