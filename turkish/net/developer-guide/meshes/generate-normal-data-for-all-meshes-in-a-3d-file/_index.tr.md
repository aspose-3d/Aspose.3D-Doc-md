---
title: 3D dosyasında tüm ağlar için normal veri oluştur
type: docs
weight: 17
url: /tr/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Using Aspose.3D for .NET, developers can generate normal data for all meshes in any 3D model (without the normal data).
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) kullanarak, geliştiriciler herhangi bir 3D modelinde (normal veri olmadan) tüm ağlar için normal veri oluşturabilirler.

{{% /alert %}}
##  **3DS dosyasında tüm ağlar için normal veri oluştur**
[`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) sınıfı tarafından maruz kalan `GenerateNormal` yöntemi, 3DS dosyasındaki tüm ağlar için normal veri oluşturmak için kullanılabilir. Eğer `VertexElementSmoothingGroup` elemanı örgüde tanımlanmışsa, oluşturulan normal veriler `VertexElementSmoothingGroup` tarafından düzeltilecektir.
###  **Programming ample ample**
Bu kod örneği 3DS dosyasını yükler, tüm düğümleri ziyaret eder ve tüm ağlar için normal veri oluşturur.

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
