---
title: Save a 3D Document in different 3D Formats using C#
linktitle: Save a 3D Document
type: docs
weight: 20
url: /net/save-a-3d-document/
description: The Scene class of the Aspose.3D API represents a 3D document and developers can save its object in any supported file format.
---

## **Overview**
The article explains how you can save 3D document in various formats using C# 3D document processing library, including

- Save a 3D Document in FBX format using C# - AutoDesk
- Save a 3D Document in DAE format using C# - Collada
- Save a 3D Document in 3DS format using C# - Discreet 3D Studio
- Save a 3D Document in DRC format using C# - Google Draco

{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D document and developers can save its object in any supported file format. To save a 3D Scene, simply use the [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) method, it accepts a file name with complete path or a file stream object. Aspose.3D API offers another `FileFormat` parameter to specify output file format.

{{% /alert %}} 

## **Save a 3D Scene in Supported 3D formats**

The C# code sample below shows how to save a 3D Scene or document to a stream in various supported 3D formats.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
