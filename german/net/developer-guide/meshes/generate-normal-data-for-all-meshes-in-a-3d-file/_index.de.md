---
title: Generieren Sie normale Daten für alle Maschen in einer 3D-Datei
type: docs
weight: 17
url: /de/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Mit Aspose.3D for .NET können Entwickler normale Daten für alle Maschen in jedem 3D-Modell generieren (ohne die normalen Daten).
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler normale Daten für alle Netze in jedem 3D-Modell generieren (ohne die normalen Daten).

{{% /alert %}}
##  **Generieren Sie normale Daten für alle Maschen in einer 3DS-Datei**
Die `GenerateNormal`-Methode, die von der [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-Klasse angezeigt wird, kann verwendet werden, um normale Daten für alle Netze in einer 3DS-Datei zu generieren. Wenn das `VertexElementSmoothingGroup`-Element im Netz definiert wurde, werden die generierten normalen Daten durch die `VertexElementSmoothingGroup` geglättet.
###  **Programmier probe**
Dieses Code beispiel lädt eine 3DS-Datei, besucht alle Knoten und erstellt normale Daten für alle Netze.

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
