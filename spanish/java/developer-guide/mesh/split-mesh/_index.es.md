---
title: Malla dividida
type: docs
weight: 10
url: /es/java/split-mesh/
description: Aspose.3D for Java API tiene soporte para dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Se puede lograr usando Aspose.3D for Java API.
---
##  **Dividir todas las mallas de escena por material**
Aspose.3D for Java API tiene soporte para dividir todas las mallas de una escena en varias submallas por material. El método SplitMesh no dividirá una malla de la escena si se le ha asignado un único material. Se puede lograr usando Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum especifica la política de datos utilizada en el algoritmo de división de malla, admite dos políticas, comparte datos entre submallas o cada submalla tiene sus propios datos (solo datos utilizados).

{{% /alert %}} 

El siguiente ejemplo de código divide todas las mallas de una escena por material. Cada sub-malla comparte los mismos datos directos y solo difiere en índices.

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
##  **Dividir una malla especificando el material**
Aspose.3D for Java API tiene soporte para dividir una malla especificando manualmente el material. La opción de dividir malla crea objetos separados y cada submalla utilizará un solo material.
###  **Malla dividida de la caja**
Este tema de ayuda crea una malla de la caja para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear una malla de cubo 3D](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Además, una caja está compuesta por 6 planos y cada plano se convertirá en una sub-malla. El ejemplo de código a continuación divide una malla primitiva especificando manualmente el material.

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
