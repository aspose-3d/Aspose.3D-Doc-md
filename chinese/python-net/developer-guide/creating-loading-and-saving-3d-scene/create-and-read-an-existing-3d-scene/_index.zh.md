---
title: 创建并读取现有 3D 场景
type: docs
weight: 10
url: /zh/python-net/create-and-read-an-existing-3d-scene/
description: Aspose。3D API 支持从头开始创建新的 3D 场景，然后以任何支持的文件格式保存。开发人员还可以加载现有的 3D 场景以进行修改、添加或处理。
---
##  **创建一个空的 3D 场景并以支持的 3D 文件格式保存**
Aspose。3D API 支持从头开始创建新的 3D 场景，然后以任何支持的文件格式保存。开发人员还可以加载现有的 3D 场景以进行修改、添加或处理。
###  **创建 3D 场景文档**
请按照以下步骤使用 Aspose.3D api创建 3D 场景文档:

1. 创建表示 3D 场景文档的 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类的实例。
1. 通过调用Scene类对象的 [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) 方法生成 3D Scene文档。
####  **创建 3D 场景文档: 编程示例**


{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.
# Create an object of the Scene class
scene = a3d.Scene()
# Save 3D scene document
scene.Save("document.fbx", a3d.FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **正在读取 3D 场景**
使用 Aspose.3D API，开发人员可以加载所有受支持的 3D 文档。的可用构造函数**场景**类允许这样做，他们接受有效的文件路径字符串。支持的可读文件格式如下:

1. FBX 7.7 (ASCII，二进制)
1. FBX 7.6 (ASCII，二进制)
1. FBX 7.5 (ASCII，二进制)
1. FBX 7.4 (ASCII，二进制)
1. FBX 7.3 (ASCII，二进制)
1. FBX 7.2 (ASCII，二进制)
1. STL (ASCII，二进制)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII，二进制)
1. X (ASCII，二进制)
1. XYZ
1. Draco
1. 3MF
1. RVM (文本，二进制)
1. ASE
1. USDZ
1. USD

`Scene` 类的构造函数在内部检测 3D 文档格式。
###  **读取 3D 场景: 编程示例**
{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.

# Initialize a Scene class object
scene = Scene()
# Load an existing 3D document
scene.open("document.fbx")


{{< /highlight >}}
