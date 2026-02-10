---
title: Spara ett 3D dokument i olika 3D format med C#
linktitle: Spara ett 3D Dokument
type: docs
weight: 20
url: /sv/net/save-a-3d-document/
description: Scenklassen för Aspose. 3D API representerar ett 3D-dokument och utvecklare kan spara objektet i vilket filformat som stöds.
---
##  **Översikt**
The article explains how you can save 3D document in various formats using C# 3D document processing library, including

- Spara ett 3D i FBX-format med C# - AutoDesk
- Spara ett 3D i DAE format med C# - Collada
- Spara ett 3D Dokument i 3DS-format med C# - Diskret 3D Studio.
- Spara ett 3D i DRC format med C# - Google Draco

{{% alert color="primary" %}} 

[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) klassen för Aspose. 3D API representerar ett 3D-dokument och utvecklare kan spara objektet i vilket filformat som stöds. För att spara en 3D scen, använd bara [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-metoden, det accepterar ett filnamn med fullständig sökväg eller ett filströmobjekt. Aspose.3D API erbjuder en annan parameter `FileFormat` för att ange utdatafilformat.

{{% /alert %}} 

##  **Spara en 3D Scen i format som stöds 3D**

Nedanstående C# kodprov visar hur en 3D Scen eller dokument ska sparas till en ström i olika format som stöds 3D s.

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
