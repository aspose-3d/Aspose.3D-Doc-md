---
title: Сплит Сетка
type: docs
weight: 10
url: /ru/java/split-mesh/
description: Aspose.3D for Java API поддерживает разделение всех ячеек сцены на несколько подячеек для каждого материала. Метод SplitMesh не будет разделять сетку сцены, если ей был назначен один материал. Это может быть достигнуто с помощью Aspose.3D for Java API.
---
##  **Разделить все сетки сцены на материал**
Aspose.3D for Java API поддерживает разделение всех ячеек сцены на несколько подячеек для каждого материала. Метод SplitMesh не будет разделять сетку сцены, если ей был назначен один материал. Это может быть достигнуто с помощью Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum определяет политику данных, используемую в алгоритме разделения ячеек, поддерживает две политики, обмениваются данными между подсетками или каждая подсетка имеет свои собственные данные (только используемые данные).

{{% /alert %}} 

Образец кода ниже разделяет все сетки сцены на материал. Каждая подсетка имеет одни и те же прямые данные и различается только по индексам.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "test.fbx";
// Load a 3D file
Scene scene = new Scene(MyDir);
// Split all meshes
PolygonModifier.splitMesh(scene, SplitMeshPolicy.CLONE_DATA);
// Save file
MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("test-splitted.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Разделите сетку, укажите материал**
Aspose.3D for Java API поддерживает разделение сетки путем указания материала вручную. Опция разделенной сетки создает отдельные объекты, и каждая подсетка будет использовать только один материал.
###  **Сплит сетка коробки**
Этот раздел справки создает сетку коробки, чтобы код был всеобъемлющим и коротким. Разработчики могут создавать сетку вручную, как рассказывают в этой теме справки: [Создайте сетку-куб 3D](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Кроме того, коробка состоит из 6 плоскостей, и каждая плоскость станет подсеткой. Приведенный ниже пример кода разбивает примитивную сетку, указывая материал вручную.

{{< highlight "java" >}}
// Create a mesh of box(A box is composed by 6 planes)
Mesh box = (new Box()).toMesh();
// Create a material element on this mesh
VertexElementMaterial mat = (VertexElementMaterial) box.createElement(VertexElementType.MATERIAL, MappingMode.POLYGON, ReferenceMode.INDEX);
// and specify different material index for each plane
mat.setIndices(new int[]{0, 1, 2, 3, 4, 5});
// Now split it into 6 sub meshes, we specified 6 different materials on each plane, each plane will become a sub mesh.
// We used the CloneData policy, each plane will has the same control point information or control point-based vertex element information.
Mesh[] planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.CLONE_DATA);
mat.getIndices().clear();
mat.setIndices(new int[]{0, 0, 0, 1, 1, 1});
// Now split it into 2 sub meshes, first mesh will contains 0/1/2 planes, and second mesh will contains the 3/4/5th planes.
// We used the CompactData policy, each plane will has its own control point information or control point-based vertex element information.
planes = PolygonModifier.splitMesh(box, SplitMeshPolicy.COMPACT_DATA);
{{< /highlight >}}
