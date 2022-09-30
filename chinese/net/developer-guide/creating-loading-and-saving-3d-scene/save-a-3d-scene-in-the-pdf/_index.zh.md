---
title: 在C#中保存PDF中的3D场景
linktitle: 在PDF中保存3D场景
type: docs
weight: 60
url: /zh/net/save-a-3d-scene-in-the-pdf/
description: Aspose.3D API的场景类表示3D场景。开发人员可以通过添加相机，灯光，多边形和其他各种实体来构建3D场景。他们现在还可以以PDF文件格式保存3D场景。
---
## **概述**

本文介绍了如何使用C# .NET 3D文件操作和转换API将3D文件转换为PDF格式，首先您需要[将3D文件加载到场景对象中](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)然后将其保存为PDF格式。它涵盖了广泛的主题，例如

- 在C#中将3D转换为PDF
- 在C#中将FBX转换为PDF
- 在C#中将STL转换为PDF
- 在C#中将U3D转换为PDF
- 在C#中将OBJ转换为PDF

{{% alert color="primary" %}} 

Aspose.3D API的[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)类表示3D场景。开发人员可以通过添加相机，灯光，多边形和其他各种实体来构建3D场景。他们现在还可以以PDF文件格式保存3D场景。

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET直接在输出文档中写入有关API和版本号的信息。例如，在将图形呈现为PDF时，Aspose.3D for .NET填充具有值 “Aspose.3D” 的`Application`字段和具有值的`PDF Producer`字段，例如 “Aspose.3D 17.9”。

请注意，您不能指示Aspose.3D for .NET API更改或从输出文档中删除此信息。

{{% /alert %}} 
## **创建带有圆柱体的3D PDF，并以阴影插图模式渲染，并使用CAD优化的照明**
`Scene`类的Save方法允许以PDF格式保存3D场景。开发人员可以加载任何3D支持的文件或构建新的3D场景，他们可以保存PDF格式的3D场景，如以下C#代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DInPdf-Save3DInPdf.cs" >}}
