---
title: Erstellen Sie Tangenten-und Binormal daten für alle Maschen in 3D Modell
type: docs
weight: 10
url: /de/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Mit Aspose.3D for Java API können Entwickler tangente und binormale Daten für alle Netze in jedem unterstützten 3D-Dokument erstellen.
---
{{% alert color="primary" %}} 

Mit Aspose.3D for Java API können Entwickler tangente und binormale Daten für alle Netze in jedem unterstützten 3D-Dokument erstellen.

{{% /alert %}} 
##  **Tangent-und Binormal-Daten für Mesh erstellen**
Wir haben zwei `buildTangentBinormal`-Methoden in der `PolygonModifier`-Klasse hinzugefügt. Eine Methode verwendet das `Scene`-Klassen objekt als Parameter und eine andere Methode das `Mesh`-Klassen objekt als Parameter, wie in diesem Code beispiel gezeigt:

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
