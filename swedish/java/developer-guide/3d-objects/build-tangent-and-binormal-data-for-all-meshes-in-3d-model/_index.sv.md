---
title: Bygg Tangent- och Binormaldata för alla meshes i 3D Modell
type: docs
weight: 10
url: /sv/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Med Aspose. 3D for Java API, utvecklare kan bygga tangent- och binormal data för alla maskor i ett dokument som stöds 3D.
---
{{% alert color="primary" %}} 

Med Aspose. 3D for Java API, utvecklare kan bygga tangent- och binormal data för alla maskor i ett dokument som stöds 3D.

{{% /alert %}} 
##  **Bygg Tangent och Binormal data för mesh**
Vi har lagt till två `buildTangentBinormal`-metoder i `PolygonModifier` klassen. En metod tar `Scene` klassobjektet som en parameter och en annan tar `Mesh` klassobjektet som en parameter som visas i den här co. Exempel:

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
