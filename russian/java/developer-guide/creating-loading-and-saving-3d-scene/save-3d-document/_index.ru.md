---
title: Сохранить документ 3D
type: docs
weight: 40
url: /ru/java/save-3d-document/
description: Aspose.3D for Java API поддерживает сохранение сцены 3D в различных типах документов 3D.
---
##  **Список поддерживаемых форматов 3D (экспорт)**
Aspose.3D for Java API поддерживает сохранение сцены 3D в различных типах документов 3D. Поддерживаемые форматы файлов для записи являются следующими:

1. FBX 7,2 (ASCII, двоичный)
1. FBX 7,3 (ASCII, двоичный)
1. FBX 7,4 (ASCII, двоичный)
1. FBX 7,5 (ASCII, двоичный)
1. STL (ASCII, двоичный)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2,0 (ASCII, двоичный)
1. RVM (Текстовый, двоичный)
##  **Экспорт документа 3D**
Aspose.3D for Java API поддерживает сохранение сцены 3D в различных типах документов 3D.
###  **Экономия сцены 3D: Примеры программирования**
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
