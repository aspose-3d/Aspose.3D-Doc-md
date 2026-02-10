---
title: 以 3D 格式添加资产信息和翻转坐标系
type: docs
weight: 10
url: /zh/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: 元数据是描述、解释、定位或使其更容易检索、使用或管理信息资源的结构化信息。Aspose.3D for Python via .NET API 允许开发人员为场景定义元数据。
---
##  **将资产信息添加到 3D 场景**
元数据是描述、解释、定位或使其更容易检索、使用或管理信息资源的结构化信息。Aspose.3D for Python via .NET API 允许开发人员为场景定义元数据。
###  **为场景定义元数据**
3D 显示产生大量元数据和图片信息。元数据是一种资产，也是节目的一部分。

1. 使用 `Scene` 类初始化 3D 场景。
1. 设置应用程序/工具名称。
1. 设置应用程序/工具供应商名称。
1. 设置测量单位。
1. 设置测量单位比例系数。
1. 以支持的文件格式保存 3D 场景。

在此示例中，我们假设场景是由名为 “Egypt” 的 CAD 工具创建的，并且由 “Manualdesk” 设计:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **以 3D 格式翻转坐标系**
Aspose.3D for Python via .NET API 允许用户以 OBJ 、 3DS 、 STL 和 U3D 格式翻转坐标系。

{{% alert color="primary" %}} 

要导入3ds文件并将其保存为 OBJ 格式，代码中将使用 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类。

{{% /alert %}} 

在此示例中，我们在导入3ds文件时翻转了坐标系，并将其保存为 OBJ 格式，而不使用材质。
