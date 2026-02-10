---
title: Generare dati normali per tutte le maglie in un file 3D
type: docs
weight: 17
url: /it/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono generare dati normali per tutte le mesh in qualsiasi modello 3D (senza i dati normali).
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori possono generare dati normali per tutte le mesh in qualsiasi modello 3D (senza i dati normali).

{{% /alert %}}
##  **Generare dati normali per tutte le maglie in un file 3DS**
Il metodo `GenerateNormal` esposto dalla classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) può essere utilizzato per generare dati normali per tutte le mesh in un file 3DS. Se l'elemento `VertexElementSmoothingGroup` è stato definito nella mesh, i dati normali generati verranno smussati da `VertexElementSmoothingGroup`.
###  **Campione di programmazione**
Questo esempio di codice carica un file 3DS, visita tutti i nodi e crea dati normali per tutte le mesh.

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
