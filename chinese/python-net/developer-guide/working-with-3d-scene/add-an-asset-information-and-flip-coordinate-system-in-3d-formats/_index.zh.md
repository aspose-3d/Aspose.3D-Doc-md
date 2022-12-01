---
title: 添加3D格式的资产信息和翻转坐标系
type: docs
weight: 10
url: /zh/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: 元数据是描述、解释、定位或更容易检索、使用或管理信息资源的结构化信息。Aspose.3D Python via .NET API允许开发人员定义场景的元数据。
---
## **将资产信息添加到3D场景**
元数据是描述、解释、定位或更容易检索、使用或管理信息资源的结构化信息。Aspose.3D Python via .NET API允许开发人员定义场景的元数据。
### **为场景定义元数据**
3D显示产生大量的元数据和图片信息。元数据是一种资产，也是节目的一部分。

1. 使用`Scene`类初始化3D场景。
1. 设置应用程序/工具名称。
1. 设置应用程序/工具供应商名称。
1. 设置测量单位。
1. 设置测量单位比例系数。
1. 以支持的文件格式保存3D场景。

在这个例子中，我们假设场景是由一个名为 “埃及” 的CAD工具创建的，它是由 “Manualdesk” 设计的:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "AssetInformation-InformationToScene-AddAssetInformationToScene.py" >}}
## **3D格式的翻转坐标系**
Python via .NET API的Aspose.3D允许用户以OBJ、3DS、STL和U3D格式翻转坐标系。

{{% alert color="primary" %}} 

要导入3ds文件并将其保存为OBJ格式，代码中使用了[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)类。

{{% /alert %}} 

在此示例中，我们在导入3ds文件时翻转了坐标系，并将其保存为OBJ格式，而没有材料。
