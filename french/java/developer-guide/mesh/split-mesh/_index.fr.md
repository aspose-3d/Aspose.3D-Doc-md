---
title: Maille fendue
type: docs
weight: 10
url: /fr/java/split-mesh/
description: Aspose.3D for Java API a le support pour diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène, si un seul matériau lui a été attribué. Cela peut être réalisé en utilisant Aspose.3D for Java API.
---
##  **Fractionnez tous les mailles de la scène par matériau**
Aspose.3D for Java API a le support pour diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène, si un seul matériau lui a été attribué. Cela peut être réalisé en utilisant Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum spécifie la politique de données utilisée dans l'algorithme de division de maillage, il prend en charge deux politiques, partage de données entre sous-maillages ou chaque sous-maillage a ses propres données (uniquement des données utilisées).

{{% /alert %}} 

L'échantillon de code ci-dessous divise toutes les mailles d'une scène par matériau. Chaque sous-maillage partage les mêmes données directes et ne diffère que dans les indices.

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
##  **Diviser un maillage en spécifiant le matériau**
Aspose.3D for Java API a le support pour diviser un maillage en spécifiant manuellement le matériau. L'option de maillage fractionné crée des objets séparés et chaque sous maillage utilisera un seul matériau.
###  **Maille fendue de la boîte**
Cette rubrique d'aide crée un maillage de la boîte pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme rapporté dans cette rubrique d'aide: [Créer un maillage de cube 3D](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). En outre, une boîte est composée de 6 plans et chaque plan deviendra un sous-maillage. L'exemple de code ci-dessous divise un maillage primitif en spécifiant manuellement le matériau.

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
