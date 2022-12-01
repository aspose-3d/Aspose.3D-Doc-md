---
title: 与气缸一起工作
type: docs
weight: 130
url: /zh/python-net/working-with-cylinder/
description: Aspose.3D Python via .NET允许定制柱面的偏移顶部。为了使用此功能，您可以使用Cylinder类的Offset属性。
---
# **自定义偏移顶部**
Aspose.3D Python via .NET允许定制柱面的偏移顶部。为了使用此功能，您可以使用`Cylinder`类的`offset`属性。下面的代码片段显示了如何自定义Offset Top:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

![todo: 图像_alt_文本](working-with-cylinder_1.png)

左边的`offset_top`设置为 (5,3，0)，很容易看到顶盖已经移动，整个躯干也受到影响。
# **自定义剪切底部**
Aspose.3D Python via .NET允许定制圆柱体的剪切底部。为了使用此功能，您可以使用`Cylinder`类的`shear_bottom`属性。下面的代码片段显示了如何自定义剪切底部:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![todo: 图像_alt_文本](working-with-cylinder_2.png)

左圆柱`shear_bottom`为 (0，0.83)，而右圆柱是序数圆柱。
# **创建风扇气缸**
Aspose.3D Python via .NET允许创建风扇气缸。为了使用此功能，您可以将`Cylinder`类的`generate_fan_cylinder`属性设置为`True`。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![todo: 图像_alt_文本](working-with-cylinder_3.png)

左气缸有`generate_fan_cylinder = False`，右气缸有`generate_fan_cylinder = True`。
