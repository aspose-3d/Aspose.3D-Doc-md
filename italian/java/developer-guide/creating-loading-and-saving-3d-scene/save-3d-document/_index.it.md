---
title: Risparmia 3D documento
type: docs
weight: 40
url: /it/java/save-3d-document/
description: Aspose.3D for Java API supporta il salvataggio di 3D in vari tipi di documenti 3D.
---
##  **Elenco dei formati supportati da 3D (esportazione)**
Aspose.3D for Java API supporta il salvataggio di 3D in vari tipi di documenti 3D. I formati di file scrivibili supportati sono i seguenti:

1. FBX 7.2 (ASCII, binario)
1. FBX 7.3 (ASCII, binario)
1. FBX 7.4 (ASCII, binario)
1. FBX 7.5 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2.0 (ASCII, Binario)
1. RVM (testo, binario)
##  **Esporta 3D documento**
Aspose.3D for Java API supporta il salvataggio di una scena 3D in vari tipi di documenti 3D.
###  **Risparmio di una scena 3D: campioni di programmazione**
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
