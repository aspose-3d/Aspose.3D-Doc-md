---
title: Spara 3D Dokumentet
type: docs
weight: 40
url: /sv/java/save-3d-document/
description: Aspose.3D for Java API har stöd för att spara 3D scen i olika typer av 3D dokument.
---
##  **Lista över format som stöds 3D (export)**
Aspose.3D for Java API har stöd för att spara 3D scen i olika typer av 3D dokument. De skrivbara filformat som stöds är följande:

1. FBX 7.2 (ASCII, Binära)
1. FBX 7.3 (ASCII, Binära)
1. FBX 7.4 (ASCII, Binära)
1. FBX 7.5 (ASCII, Binära)
1. STL (ASCII, binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2.0 (ASCII, binärt)
1. RVM (Text, binärt)
##  **Exportera 3D dokument**
Aspose.3D for Java API har stöd för att spara en 3D scen i olika typer av 3D dokument.
###  **Spara en 3D Scene: Programmeringsprovning**
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
