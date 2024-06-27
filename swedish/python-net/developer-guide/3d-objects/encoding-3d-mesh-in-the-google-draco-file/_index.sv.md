---
title: Kodning 3D Mesh i Google Draco filen
type: docs
weight: 60
url: /sv/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Python via .NET API tillåter utvecklare att importera en 3D-modell, och koda maskor i Google Draco filerna. Utvecklare kan också ange position, struktur koordinater, färg och normala bitar samt komprimeringsnivå innan kodning av en mesh.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API allows developers to [import a 3D model](/3d/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.

{{% /alert %}}
##  **Hämta en 3D Mesh och koda i Google Draco fil**
Den `encode`-metod som exponeras av [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-klassen kan användas för att koda en 3D-mash i Google-filen Draco. Det tar ett [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) och [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) objekt som parametrar. Med Draco sparningsalternativ kan utvecklare också ange position, texturkoordinater, färg och normala bitar samt kompressionsnivå före kodning av en mesh.
###  **Programmeringsprova**
Detta kodexempel hämtar en Mesh of Sphere, och koda sedan i filen Google Draco efter att en komprimeringsnivå har angetts.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
