---
title: Tüm poligonları 3D modelinde üçgenlere dönüştürün
type: docs
weight: 10
url: /tr/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API tüm poligonları desteklenen herhangi bir 3D belgesinde üçgenlere dönüştürme desteğine sahiptir.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tüm poligonları desteklenen herhangi bir 3D belgesinde üçgenlere dönüştürme desteğine sahiptir.

{{% /alert %}} 
##  **Tonvert tüm olyolygons Triangles**
Bu kod örneğinde gösterildiği gibi bir parametre olarak `Scene` sınıf nesnesini alan `PolygonModifier` sınıfında başka bir triangulate yöntemi aşırı yükledik:

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
