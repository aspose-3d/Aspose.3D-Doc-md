---
title: 创建和读取现有3D场景
type: docs
weight: 10
url: /zh/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API支持从头开始创建新的3D场景，然后以任何受支持的文件格式保存。开发人员还可以加载现有3D场景以用于修改、添加或处理目的。
---
## **创建一个空3D场景并以支持的3D文件格式保存**
Aspose.3D API支持从头开始创建新的3D场景，然后以任何受支持的文件格式保存。开发人员还可以加载现有3D场景以用于修改、添加或处理目的。
### **创建3D场景文档**
请按照以下步骤使用Aspose.3D api创建3D场景文档:

1. 创建表示3D场景文档的[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)类的实例。
1. 通过调用场景类对象的[`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)方法生成3D场景文档。
#### **创建3D场景文档: 编程示例**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
## **阅读3D场景**
使用Aspose.3D API，开发人员可以加载所有支持的3D文档。的可用构造函数**场景**类允许这样做，他们接受有效的文件路径字符串。支持的可读文件格式如下:

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

`Scene`类的构造函数在内部检测3D文档格式。
### **阅读3D场景: 编程示例**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
