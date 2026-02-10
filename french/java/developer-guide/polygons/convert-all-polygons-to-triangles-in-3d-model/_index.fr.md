---
title: Convertir tous les polygones en triangles dans le modèle 3D
type: docs
weight: 10
url: /fr/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API a le support de la conversion de tous les polygones en triangles dans tout document 3D supporté.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API a le support de la conversion de tous les polygones en triangles dans tout document 3D supporté.

{{% /alert %}} 
##  **Convertir tous les Polygones en Triangles**
Nous avons ajouté une autre surcharge de la méthode de triangulation dans la classe `PolygonModifier` qui prend un objet de classe `Scene` comme paramètre comme indiqué dans cet exemple de code:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene(MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.triangulate(scene);
// Save 3D scene
scene.save(MyDir + "triangulated_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
