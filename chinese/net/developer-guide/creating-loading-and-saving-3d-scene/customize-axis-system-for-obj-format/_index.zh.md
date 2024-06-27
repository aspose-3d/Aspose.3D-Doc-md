---
title: 自定义obj格式的轴系
linktitle: 在将场景导出为 OBJ 格式的过程中自定义轴系
type: docs
weight: 70
url: /zh/net/customize-axis-system-for-obj-format
description: OBJ 没有默认坐标系，我们可以为其手动定义轴系。
---
{{% alert color="primary" %}} 

Wavefront OBJ 文件不遵循标准坐标系; 相反，解释通常由导入器处理。但是，[Aspose.3D for .NET](https://products.aspose.com/3d/net/) 提供了为 OBJ 文件手动指定轴系的灵活性。这包括定义上轴和前轴以及在左手坐标系和右手坐标系之间进行选择。Aspose.3D 将自动处理坐标系转换，确保您的 3D 模型的一致性和准确性。


{{% /alert %}} 
##  **正在为 Aspose 中的 OBJ 个文件指定轴系统。3D**

以下是在 Aspose 中处理 OBJ 文件时手动设置轴系的方法。3D:

{{< highlight "csharp" >}}
//construct a right-handed axis system with +y as up and -z as front
Axis up = Axis.YAxis;
Axis front = Axis.NegativeZAxis;
AxisSystem axisSystem = new AxisSystem(CoordinateSystem.RightHanded, up, front);

ObjSaveOptions opt = new ObjSaveOptions();
//use the custom axis system to flip coordinate
opt.AxisSystem = axisSystem;
//set this to true, will convert mesh's position/normal from source axis system to custom axis system
//source axis system is defined by scene.AssetInfo.CoordinateSystem, scene.AssetInfo.UpVector, scene.AssetInfo.FrontVector
opt.FlipCoordinateSystem = true;

 // initialize a new 3D scene from existing file

var scene = Scene.FromFile("input.dae");

// Save the scene with customized axis system
s.Save("output.obj", opt);

{{< /highlight >}}

通过对 OBJ 文件使用 Aspose.3D 的轴系配置，无论 OBJ 文件中使用的原始坐标系如何，都可以获得一致且准确的导入结果。此功能增强了灵活性和控制力，使您可以更轻松地在各种 3D 工作流程中集成和使用 OBJ 文件。

##  **资源**

1. [在线教程](https://products.aspose.com/3d/tutorial/)
2. [轴系](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)