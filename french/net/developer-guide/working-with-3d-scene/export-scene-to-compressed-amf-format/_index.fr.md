---
title: Exporter la scène au format compressé AMF
type: docs
weight: 30
url: /fr/net/export-scene-to-compressed-amf-format/
description: Aspose.3D for .NET offre la classe AmfSaveOptions qui vous permet de définir la valeur bool pour la compression selon vos besoins. Par défaut, la valeur est définie sur true.
---
##  **Exporter la scène au format compressé AMF**
Aspose.3D for .NET offre une classe `AmfSaveOptions` qui vous permet de définir la valeur bool pour la compression selon vos besoins. Par défaut, la valeur est définie sur true. L'extrait de code suivant montre la fonctionnalité complète pour générer un fichier au format AMF compressé:

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
