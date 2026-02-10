---
title: 保存 3D 文档
type: docs
weight: 40
url: /zh/java/save-3d-document/
description: Aspose.3D for Java API 支持将 3D 场景保存在各种类型的 3D 文档中。
---
##  **3D 支持的格式列表 (导出)**
Aspose.3D for Java API 支持将 3D 场景保存在各种类型的 3D 文档中。支持的可写文件格式如下:

1. FBX 7.2 (ASCII，二进制)
1. FBX 7.3 (ASCII，二进制)
1. FBX 7.4 (ASCII，二进制)
1. FBX 7.5 (ASCII，二进制)
1. STL (ASCII，二进制)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. GLB
1. Draco
1. GLTF 2.0 (ASCII，二进制)
1. RVM (文本，二进制)
##  **导出 3D 文档**
Aspose.3D for Java API 支持将 3D 场景保存在各种类型的 3D 文档中。
###  **保存 3D 场景: 编程示例**
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
