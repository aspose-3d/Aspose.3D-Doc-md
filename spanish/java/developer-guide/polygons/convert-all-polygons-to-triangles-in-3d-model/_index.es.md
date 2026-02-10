---
title: Convertir todos los polígonos a triángulos en el modelo 3D
type: docs
weight: 10
url: /es/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API tiene soporte para convertir todos los polígonos a triángulos en cualquier documento 3D soportado.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte para convertir todos los polígonos a triángulos en cualquier documento 3D soportado.

{{% /alert %}} 
##  **Convertir todos los polígonos a Triángulos**
Hemos agregado otra sobrecarga del método triangular en la clase `PolygonModifier` que toma un objeto de clase `Scene` como un parámetro como se muestra en este ejemplo de código:

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
