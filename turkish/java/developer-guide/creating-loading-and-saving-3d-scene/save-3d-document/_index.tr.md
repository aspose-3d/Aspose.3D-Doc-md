---
title: Save 3D Document
type: docs
weight: 40
url: /tr/java/save-3d-document/
description: Aspose.3D for Java API has support of saving 3D scene in various type of 3D documents.
---
##  **3D desteklenen formatların listesi (İhracat)**
Aspose.3D for Java API has support of saving 3D scene in various type of 3D documents. The supported writable file formats are as follows:

1. FBX 7.2 (ascii, ikili)
1. FBX 7.3 (ascii, İkili)
1. FBX 7.4 (ascii, ikili)
1. FBX 7.5 (ascii, ikili)
1. STL (ascii, ikili)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2.0 (ascii, ikili)
1. RVM (metin, ikili)
##  **Export 3D document**
Aspose.3D for Java API has support of saving a 3D scene in various types of 3D document.
###  **3D sahne tasarrufu: programlama örnekleri**
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
