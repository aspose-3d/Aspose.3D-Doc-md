---
title: وفِّر 3D مستند
type: docs
weight: 40
url: /ar/java/save-3d-document/
description: Aspose.3D for Java API يدعم توفير مشهد 3D في أنواع مختلفة من مستندات 3D.
---
##  **قائمة الصيغ المدعومة بقيمة 3D (تصدير)**
Aspose.3D for Java API يدعم توفير مشهد 3D في أنواع مختلفة من مستندات 3D. تنسيقات الملفات القابلة للكتابة المدعومة هي كما يلي:

1. FBX 7.2 (ASCII ، ثنائي)
1. FBX 7.3 (ASCII ، ثنائي)
1. FBX 7.4 (ASCII ، ثنائي)
1. FBX 7.5 (ASCII ، ثنائي)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2.0 (ASCII ، ثنائي)
1. RVM (Text, Binary)
##  **تصدير مستند 3D**
Aspose.3D for Java API يدعم توفير مشهد 3D في أنواع مختلفة من مستندات 3D.
###  **توفير مشهد 3D: عينات برمجة**
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
