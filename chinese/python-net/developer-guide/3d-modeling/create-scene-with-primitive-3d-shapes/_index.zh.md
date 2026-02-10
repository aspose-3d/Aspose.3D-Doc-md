---
title: 创建具有原始 3D 形状的场景
type: docs
weight: 10
url: /zh/python-net/create-scene-with-primitive-3d-shapes/
description: 使用 Aspose.3D for Python via .NET，开发人员可以定义具有原始 3D 形状的场景。所有参数化图元将自动转换为网格，同时以任何支持的输出文件格式保存。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/)，开发人员可以定义具有原始 3D 形状的场景。所有参数化图元将自动转换为网格，同时以任何支持的输出文件格式保存。

{{% /alert %}}
##  **从原始 3D 形状生成场景**
建模是纯粹的创建过程，Aspose.3D API 支持创建具有原始 3D 形状的场景。
###  **编程示例**
此代码示例创建一个包含原始 3D 形状的场景，并将其保存在 FBX 文件中。

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Box, Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
#  Initialize a Scene object
scene = Scene()
#  Create a Box model
scene.root_node.create_child_node("box", Box())
#  Create a Cylinder model
scene.root_node.create_child_node("cylinder", Cylinder())
#  Save drawing in the FBX format
output = "out"  + "test.fbx"
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
