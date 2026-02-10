---
title: Преобразовать все многоугольники в треугольники в модели 3D
type: docs
weight: 10
url: /ru/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API поддерживает преобразование всех полигонов в треугольники в любом поддерживаемым 3D документе.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API поддерживает преобразование всех полигонов в треугольники в любом поддерживаемым 3D документе.

{{% /alert %}} 
##  **Конвертировать все полигоны в треугольники**
Мы добавили еще одну перегрузку триангулятного метода в классе `PolygonModifier`, который принимает объект класса `Scene` в качестве параметра, как показано в этом примере кода:

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
