---
title: Générer des données normales pour tous les maillages dans un fichier 3D
type: docs
weight: 17
url: /fr/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: En utilisant Aspose.3D for .NET, les développeurs peuvent générer des données normales pour tous les maillages dans n'importe quel modèle 3D (sans les données normales).
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs peuvent générer des données normales pour tous les maillages dans n'importe quel modèle 3D (sans les données normales).

{{% /alert %}}
##  **Générer des données normales pour tous les maillages dans un fichier 3DS**
La méthode `GenerateNormal` exposée par la classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) peut être utilisée pour générer des données normales pour tous les maillages d'un fichier 3DS. Si l'élément `VertexElementSmoothingGroup` a été défini dans le maillage, les données normales générées seront lissées par le `VertexElementSmoothingGroup`.
###  **Échantillon de programmation**
Cet exemple de code charge un fichier 3DS, visite tous les nœuds et crée des données normales pour tous les maillages.

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
