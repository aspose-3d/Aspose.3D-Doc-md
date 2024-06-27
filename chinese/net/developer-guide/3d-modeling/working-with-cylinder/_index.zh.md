---
title: 与气缸一起工作
type: docs
weight: 130
url: /zh/net/working-with-cylinder/
description: Aspose.3D for .NET 允许自定义圆柱体的偏移顶部。为了使用此功能，可以使用Cylinder类的Offset属性。
---
#  **自定义偏移顶部**
Aspose.3D for .NET 允许自定义圆柱体的偏移顶部。为了使用此功能，您可以使用 `Cylinder` 类的 `Offset` 属性。以下代码段显示了如何自定义偏移顶部:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

![todo: 图像 _ alt_text](working-with-cylinder_1.png)

左边的OffsetTop设置为 (5,3，0)，很容易看到顶盖移动了，整个躯干也受到了影响。
#  **自定义剪切底部**
Aspose.3D for .NET 允许自定义圆柱体的剪切底部。为了使用此功能，您可以使用 `Cylinder` 类的 `ShearBottom` 属性。以下代码段显示了如何自定义剪切底部:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

![todo: 图像 _ alt_text](working-with-cylinder_2.png)

左侧圆柱体有 `ShearBottom` 到 (0，0.83)，而右侧圆柱体是一个有序圆柱体。
#  **创建风扇气缸**
Aspose.3D for .NET 允许创建风扇圆柱体。为了使用此功能，您可以将 `Cylinder` 类的 `GenerateFanCylinder` 属性设置为 `true`。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

![todo: 图像 _ alt_text](working-with-cylinder_3.png)

左侧气缸有 `GenerateFanCylinder = false`，右侧气缸有 `GenerateFanCylinder = true`。
