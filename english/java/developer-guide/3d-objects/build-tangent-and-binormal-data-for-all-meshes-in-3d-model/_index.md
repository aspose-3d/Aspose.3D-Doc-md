---
title: Build Tangent and Binormal data for all Meshes in 3D Model
type: docs
weight: 10
url: /java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: With Aspose.3D for Java API, developers can build tangent and binormal data for all meshes in any supported 3D document.
---

{{% alert color="primary" %}} 

With Aspose.3D for Java API, developers can build tangent and binormal data for all meshes in any supported 3D document.

{{% /alert %}} 
## **Build Tangent and Binormal data for Mesh**
We have added two `buildTangentBinormal` methods in the `PolygonModifier` class. One method takes the `Scene` class object as a parameter and another one takes the `Mesh` class object as a parameter as shown in this code example:

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
