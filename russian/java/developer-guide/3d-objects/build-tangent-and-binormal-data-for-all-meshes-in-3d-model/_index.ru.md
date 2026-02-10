---
title: Построение касательных и бинонормальных данных для всех ячеек в модели 3D
type: docs
weight: 10
url: /ru/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: С помощью Aspose.3D for Java API разработчики могут создавать касательные и бинонормальные данные для всех ячеек в любом поддерживаемым 3D документе.
---
{{% alert color="primary" %}} 

С помощью Aspose.3D for Java API разработчики могут создавать касательные и бинонормальные данные для всех ячеек в любом поддерживаемым 3D документе.

{{% /alert %}} 
##  **Построить Tangent и Binormal данные для Mesh**
Мы добавили два метода `buildTangentBinormal` в класс `PolygonModifier`. Один метод принимает объект класса `Scene` в качестве параметра, а другой-объект класса `Mesh` в качестве параметра, как показано в этом примере кода:

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
