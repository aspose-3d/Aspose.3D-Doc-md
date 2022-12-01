---
title: 创建和读取现有3D场景
type: docs
weight: 10
url: /zh/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API支持从头开始创建新的3D场景，然后以任何受支持的文件格式保存。开发人员还可以加载现有3D场景以用于修改、添加或处理目的。
---
## **概述**
本文介绍了使用C# 3D文件格式操作库的以下主题。
- 从头开始在C#中创建一个空3D场景
- 在C#中读取或加载现有3D场景
- 使用C#将3D场景保存为支持的3D格式
- 在C#中使用3D场景属性

## **创建一个空3D场景并以支持的3D文件格式保存**
Aspose.3D API支持从头开始创建新的3D场景，然后以任何受支持的文件格式保存。开发人员还可以加载现有3D场景以用于修改、添加或处理目的。

### **创建3D场景文档**
请按照以下步骤C#使用Aspose.3D api创建3D场景文档:

1. 创建表示3D场景文档的[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)类的实例。
1. 通过调用场景类对象的[`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)方法生成3D场景文档。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

## **阅读3D场景**
使用Aspose.3D API，开发人员可以加载所有支持的3D文档。`Scene`类的可用构造函数允许这样做，并且它们接受有效的文件路径字符串。支持的可读文件格式如下:

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
1. Draco
1. 3MF
1. RVM (文本，二进制)
1. ASE

`Scene`类的构造函数在内部检测3D文档格式。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

## **使用3D场景属性**
Aspose.3D API使您可以使用场景的子节点读取3D场景属性。下面的C#代码示例演示了此功能的用法。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
