---
title: Skapa normala data för alla maskor i en 3D fil
type: docs
weight: 70
url: /sv/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Med Aspose.3D for Python via .NET kan utvecklare generera normala data för alla maskor i en 3D-modell (utan normala data).
---
{{% alert color="primary" %}}

Med [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) kan utvecklare generera normala data för alla maskor i en 3D-modell (utan normala data).

{{% /alert %}}
##  **Skapa normala data för alla maskor i en 3DS fil**
Den `generate_normal`-metod som exponeras av [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-klassen kan användas för att skapa normala data för alla maskor i en 3DS-fil. Om `VertexElementSmoothingGroup` element definierades i mesh, kommer den genererade normala data att jämnas ut av `VertexElementSmoothingGroup`.
###  **Programmeringsprova**
Det här kodexemplet laddar en 3DS-fil, besöker alla noder och skapar normala data för alla maskor.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
