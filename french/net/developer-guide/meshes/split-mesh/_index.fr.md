---
title: Maille fendue
type: docs
weight: 100
url: /fr/net/split-mesh/
description: Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant Aspose.3D for .NET API.
---
##  **Divisez tous les mailles d'une scène par matériau**
Les développeurs peuvent avoir besoin de diviser tous les maillages d'une scène en plusieurs sous-maillages par matériau. La méthode SplitMesh ne divise pas un maillage de la scène si un seul matériau lui a été attribué. Les développeurs peuvent maintenant y parvenir en utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum spécifie la politique de données utilisée dans l'algorithme de division de maillage, il prend en charge deux politiques, partage de données entre sous-maillages ou chaque sous-maillage a ses propres données (uniquement des données utilisées).

{{% /alert %}}

L'échantillon de code ci-dessous divise toutes les mailles d'une scène par matériau. Chaque sous-maillage partage les mêmes données directes et ne diffère que dans les indices.

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
##  **Diviser un maillage en spécifiant le matériau**
Aspose.3D for .NET API permet aux développeurs de diviser un maillage en spécifiant manuellement le matériau. L'option de maillage fractionné crée des objets séparés et chaque sous maillage utilisera un seul matériau.
###  **Fendre la maille de la boîte**
Cette rubrique d'aide crée un maillage de la boîte pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme rapporté dans cette rubrique d'aide: [Créer un maillage de cube 3D](/3d/fr/net/create-3d-mesh-and-scene/). En outre, une boîte est composée de 6 plans et chaque plan deviendra un sous-maillage. L'exemple de code ci-dessous divise un maillage primitif en spécifiant manuellement le matériau.

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
