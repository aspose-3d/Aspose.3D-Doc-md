---
title: 与气缸一起工作
type: docs
weight: 130
url: /zh/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET 允许自定义圆柱体的偏移顶部。为了使用此功能，可以使用Cylinder类的Offset属性。
---
#  **自定义偏移顶部**
Aspose.3D for Python via .NET 允许自定义圆柱体的偏移顶部。为了使用此功能，您可以使用 `Cylinder` 类的 `offset` 属性。以下代码段显示了如何自定义偏移顶部:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

![todo: 图像 _ alt_text](working-with-cylinder_1.png)

左边的 `offset_top` 设置为 (5，3，0)，很容易看到顶帽已经移动，整个躯干也受到影响。
#  **自定义剪切底部**
Aspose.3D for Python via .NET 允许自定义圆柱体的剪切底部。为了使用此功能，您可以使用 `Cylinder` 类的 `shear_bottom` 属性。以下代码段显示了如何自定义剪切底部:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![todo: 图像 _ alt_text](working-with-cylinder_2.png)

左侧圆柱体有 `shear_bottom` 到 (0，0.83)，而右侧圆柱体是一个有序圆柱体。
#  **创建风扇气缸**
Aspose.3D for Python via .NET 允许创建一个风扇圆柱体。为了使用此功能，您可以将 `Cylinder` 类的 `generate_fan_cylinder` 属性设置为 `True`。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![todo: 图像 _ alt_text](working-with-cylinder_3.png)

左侧气缸有 `generate_fan_cylinder = False`，右侧气缸有 `generate_fan_cylinder = True`。
