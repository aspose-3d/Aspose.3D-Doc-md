---
title: Construire des données tangentes et binormales pour tous les maillages dans le modèle 3D
type: docs
weight: 10
url: /fr/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Avec Aspose.3D for Java API, les développeurs peuvent construire des données tangentes et binormales pour tous les maillages de tout document 3D pris en charge.
---
{{% alert color="primary" %}} 

Avec Aspose.3D for Java API, les développeurs peuvent construire des données tangentes et binormales pour tous les maillages de tout document 3D pris en charge.

{{% /alert %}} 
##  **Construire des données Tangent et Binormal pour Mesh**
Nous avons ajouté deux méthodes `buildTangentBinormal` dans la classe `PolygonModifier`. Une méthode prend l'objet de classe `Scene` comme paramètre et une autre prend l'objet de classe `Mesh` comme paramètre comme indiqué dans cet exemple de code:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene( MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.buildTangentBinormal(scene);
// Save 3D scene
scene.save(MyDir + "BuildTangentAndBinormalData_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
