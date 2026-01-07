---
title: 阅读3D文档
type: docs
weight: 30
url: "/zh/nodejs-java/read-3d-document/"
description: Aspose.3D for Node.js 通过 Java API 支持读取各种类型的 3D 文档。
---

## **支持的 3D 格式列表（导入）**
Aspose.3D for Node.js via Java API 支持读取各种类型的 3D 文档。`Scene` 类的可用构造函数可以实现此目的，它们接受有效的文件路径字符串。支持的可读文件格式如下：

1. FBX 7.5 (ASCII, Binary)
1. FBX 7.4 (ASCII, Binary)
1. FBX 7.3 (ASCII, Binary)
1. FBX 7.2 (ASCII, Binary)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCII, Binary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

Scene 类的构造函数内部检测 3D 文档格式。
## **导入 3D 文档**
Aspose.3D for Java API 支持导入各种类型的 3D 文档，用于修改、添加和处理。
### **读取 3D 场景：编程示例**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化一个 Scene 类对象
var scene = new aspose.threed.Scene();

// 加载现有的 3D 文档
scene.open( "document.obj");

{{< /highlight >}}