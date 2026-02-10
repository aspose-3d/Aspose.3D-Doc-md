---
title: Guardar documento 3D
type: docs
weight: 40
url: /es/java/save-3d-document/
description: Aspose.3D for Java API tiene soporte para guardar la escena 3D en varios tipos de documentos 3D.
---
##  **Lista de formatos compatibles con 3D (export)**
Aspose.3D for Java API tiene soporte para guardar la escena 3D en varios tipos de documentos 3D. Los formatos de archivo de escritura admitidos son los siguientes:

1. FBX 7,2 (ASCII, binario)
1. FBX 7,3 (ASCII, binario)
1. FBX 7,4 (ASCII, binario)
1. FBX 7,5 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2,0 (ASCII, binario)
1. RVM (Texto, binario)
##  **Exportar documento 3D**
Aspose.3D for Java API tiene soporte para guardar una escena 3D en varios tipos de documentos 3D.
###  **Guardar una escena 3D: Muestras de programación**
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
