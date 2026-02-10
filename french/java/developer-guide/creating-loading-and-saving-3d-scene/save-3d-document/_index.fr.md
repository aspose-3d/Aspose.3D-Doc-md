---
title: Économisez 3D Document
type: docs
weight: 40
url: /fr/java/save-3d-document/
description: Aspose.3D for Java API a le support de la sauvegarde de la scène 3D dans divers types de documents 3D.
---
##  **Liste des formats supportés par 3D (exportation)**
Aspose.3D for Java API a le support de la sauvegarde de la scène 3D dans divers types de documents 3D. Les formats de fichiers accessibles en écriture pris en charge sont les suivants:

1. FBX 7.2 (ASCII, binaire)
1. FBX 7.3 (ASCII, binaire)
1. FBX 7.4 (ASCII, binaire)
1. FBX 7.5 (ASCII, binaire)
1. STL (ASCII, binaire)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2.0 (ASCII, binaire)
1. RVM (Texte, Binaire)
##  **Exporter le document 3D**
Aspose.3D for Java API permet d'enregistrer une scène 3D dans différents types de documents 3D.
###  **Enregistrer une scène 3D: Programmation des échantillons**
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
