---
title: Construir datos tangentes y binormales para todas las mallas en el modelo 3D
type: docs
weight: 10
url: /es/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Con Aspose.3D for Java API, los desarrolladores pueden crear datos tangentes y binormales para todas las mallas en cualquier documento 3D compatible.
---
{{% alert color="primary" %}} 

Con Aspose.3D for Java API, los desarrolladores pueden crear datos tangentes y binormales para todas las mallas en cualquier documento 3D compatible.

{{% /alert %}} 
##  **Construir datos tangentes y binormales para malla**
Hemos agregado dos métodos `buildTangentBinormal` en la clase `PolygonModifier`. Un método toma el objeto de clase `Scene` como un parámetro y otro toma el objeto de clase `Mesh` como un parámetro como se muestra en este ejemplo de código:

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
