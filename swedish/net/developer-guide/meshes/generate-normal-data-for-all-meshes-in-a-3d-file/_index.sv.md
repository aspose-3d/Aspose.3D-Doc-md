---
title: Skapa normala data för alla maskor i en 3D fil
type: docs
weight: 17
url: /sv/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Använder Aspose. 3D for .NET, kan utvecklare generera normala data för alla maskor i en 3D-modell (utan normala data).
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET](https://products.aspose.com/3d/net/) kan utvecklare generera normala data för alla maskor i en 3D-modell (utan normala data).

{{% /alert %}}
##  **Skapa normala data för alla maskor i en 3DS fil**
Den `GenerateNormal`-metod som exponeras av [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-klassen kan användas för att skapa normala data för alla maskor i en 3DS-fil. Om `VertexElementSmoothingGroup` element definierades i mesh, kommer den genererade normala data att jämnas ut av `VertexElementSmoothingGroup`.
###  **Programmeringsprova**
Det här kodexemplet laddar en 3DS-fil, besöker alla noder och skapar normala data för alla maskor.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3ds file, 3ds file doesn't have normal data, but it has smoothing group
            Scene s = new Scene(RunExamples.GetDataFilePath("camera.3ds"));
            // Visit all nodes and create normal data for all meshes
            s.RootNode.Accept(delegate(Node n)
            {
                Mesh mesh = n.GetEntity<Mesh>();
                if (mesh != null)
                {
                    VertexElementNormal normals = PolygonModifier.GenerateNormal(mesh);
                    mesh.VertexElements.Add(normals);
                }
                return true;
            });

{{< /highlight >}}
