---
title: Kodning 3D Mesh i Google Draco filen
type: docs
weight: 60
url: /sv/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API allows developers to import a 3D model, and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API allows developers to [import a 3D model](/3d/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.

{{% /alert %}}
##  **Hämta en 3D Mesh och koda i Google Draco fil**
Den `Encode`-metod som exponeras av [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-klassen kan användas för att koda en 3D-mash i Google-filen Draco. Det tar ett [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) och [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) objekt som parametrar. Med Draco sparningsalternativ kan utvecklare också ange position, texturkoordinater, färg och normala bitar samt kompressionsnivå före kodning av en mesh.
###  **Programmeringsprova**
Det här kodexemplet hämtar en `Mesh` för `Sphere`, och koda sedan i Google Draco filen efter en komprimeringsnivå.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.cs" >}}
