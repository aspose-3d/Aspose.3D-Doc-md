---
title: 3D Dokument sparen
type: docs
weight: 40
url: /de/java/save-3d-document/
description: Aspose.3D for Java API bietet Unterstützung für das Speichern von 3D-Szenen in verschiedenen Arten von 3D-Dokumenten.
---
##  **Liste der von 3D unterstützten Formate (Export)**
Aspose.3D for Java API bietet Unterstützung für das Speichern von 3D-Szenen in verschiedenen Arten von 3D-Dokumenten. Die unterstützten beschreibbaren Dateiformate lauten wie folgt:

1. FBX 7.2 (ASCII, Binär)
1. FBX 7.3 (ASCII, Binär)
1. FBX 7.4 (ASCII, Binär)
1. FBX 7.5 (ASCII, Binär)
1. STL (ASCII, Binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2.0 (ASCII, Binär)
1. RVM (Text, Binär)
##  **3D-Dokument exportieren**
Aspose.3D for Java API unterstützt das Speichern einer 3D-Szene in verschiedenen Arten von 3D-Dokumenten.
###  **Speichern einer 3D-Szene: Samples programmieren**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load a 3D document into Aspose.3D
Scene scene = new Scene();
// Open an existing 3D scene
scene.open(MyDir + "document.fbx");
// Save Scene to a stream
try (MemoryStream dstStream = new MemoryStream()) {
    scene.save(dstStream, FileFormat.FBX7500ASCII);
}
// Save Scene to a local path
scene.save(MyDir + "output_out.fbx", FileFormat.FBX7500ASCII);
{{< /highlight >}}
