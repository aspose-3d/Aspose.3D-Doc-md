---
title: Rete spaccata
type: docs
weight: 10
url: /it/java/split-mesh/
description: Aspose.3D for Java API supporta la suddivisione di tutte le maglie di una scena in diverse mesh secondarie per materiale. Il metodo SplitMesh non dividerà una mesh della scena, se gli è stato assegnato un singolo materiale. Può essere ottenuto utilizzando Aspose.3D for Java API.
---
##  **Dividi tutte le maglie della scena per materiale**
Aspose.3D for Java API supporta la suddivisione di tutte le maglie di una scena in diverse mesh secondarie per materiale. Il metodo SplitMesh non dividerà una mesh della scena, se gli è stato assegnato un singolo materiale. Può essere ottenuto utilizzando Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum specifica la politica dei dati utilizzata nell'algoritmo di frazionamento mesh, supporta due criteri, condividi i dati tra sottogruppi o ogni sottorete ha i propri dati (solo dati utilizzati).

{{% /alert %}} 

Il codice di esempio seguente divide tutte le mesh di una scena per materiale. Ogni sottogmesh condivide gli stessi dati diretti e differisce solo negli indici.

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
##  **Dividi una maglia specificando il materiale**
Aspose.3D for Java API supporta la divisione di una mesh specificando manualmente il materiale. L'opzione split mesh crea oggetti separati e ogni sottogmesh utilizzerà un solo materiale.
###  **Rete spaccata della scatola**
Questo argomento di aiuto crea una mesh della casella per mantenere il codice completo e breve. Gli sviluppatori possono costruire una mesh manualmente come narrato in questo argomento di aiuto: [Crea una mesh cubica da 3D](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Inoltre, una scatola è composta da 6 aerei e ogni aereo diventerà una sub mesh. Il codice di esempio seguente divide una mesh primitiva specificando manualmente il materiale.

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
