---
title: Сплит Сетка
type: docs
weight: 100
url: /ru/net/split-mesh/
description: Разработчикам может потребоваться разделить все сетки сцены на несколько подячеек для каждого материала. Метод SplitMesh не будет разделять сетку сцены, если ей был назначен один материал. Теперь разработчики могут достичь этого, используя Aspose.3D for .NET API.
---
##  **Разделите все сетки сцены на материал**
Разработчикам может потребоваться разделить все сетки сцены на несколько подячеек для каждого материала. Метод SplitMesh не будет разделять сетку сцены, если ей был назначен один материал. Теперь разработчики могут достичь этого, используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum определяет политику данных, используемую в алгоритме разделения ячеек, поддерживает две политики, обмениваются данными между подсетками или каждая подсетка имеет свои собственные данные (только используемые данные).

{{% /alert %}}

Образец кода ниже разделяет все сетки сцены на материал. Каждая подсетка имеет одни и те же прямые данные и различается только по индексам.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
string input = RunExamples.GetDataFilePath("test.fbx");

// Load a 3D file
Scene scene = new Scene(input);
// Split all meshes
PolygonModifier.SplitMesh(scene, SplitMeshPolicy.CloneData);

// Save file
var output = RunExamples.GetOutputFilePath("test-splitted.fbx");
scene.Save(output, FileFormat.FBX7500ASCII);


{{< /highlight >}}
##  **Разделите сетку, укажите материал**
Aspose.3D for .NET API позволяет разработчикам разделить сетку, указав материал вручную. Опция разделенной сетки создает отдельные объекты, и каждая подсетка будет использовать только один материал.
###  **Разделите сетку коробки**
Этот раздел справки создает сетку коробки, чтобы код был всеобъемлющим и коротким. Разработчики могут создавать сетку вручную, как рассказывают в этой теме справки: [Создайте сетку-куб 3D](/3d/ru/net/create-3d-mesh-and-scene/). Кроме того, коробка состоит из 6 плоскостей, и каждая плоскость станет подсеткой. Приведенный ниже пример кода разбит примитивную сетку, указывая материал вручную.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a mesh of box(A box is composed by 6 planes)
            Mesh box = (new Box()).ToMesh();
            // Create a material element on this mesh
            VertexElementMaterial mat = (VertexElementMaterial)box.CreateElement(VertexElementType.Material, MappingMode.Polygon, ReferenceMode.Index);
            // And specify different material index for each plane
            mat.Indices.AddRange(new int[] { 0, 1, 2, 3, 4, 5 });
            // Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
            // We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
            Mesh[] planes = PolygonModifier.SplitMesh(box, SplitMeshPolicy.CloneData);

            mat.Indices.Clear();
            mat.Indices.AddRange(new int[] { 0, 0, 0, 1, 1, 1 });
            // Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
            // We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
            planes = PolygonModifier.SplitMesh(box, SplitMeshPolicy.CompactData);


{{< /highlight >}}
