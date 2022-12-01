---
title: 与气缸一起工作
type: docs
weight: 100
url: /zh/java/working-with-cylinder/
description: Aspose.3D for Java允许自定义柱面的偏移顶部。为了使用此功能，您可以使用Cylinder类的setOffsetTop() 方法。
---
# **自定义偏移顶部**
Aspose.3D for Java允许自定义柱面的偏移顶部。为了使用此功能，您可以使用`Cylinder`类的`setOffsetTop()`方法。下面的代码片段显示了如何自定义Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

![todo: 图像_alt_文本](working-with-cylinder_1.png)

左边的OffsetTop设置为 (5,3，0)，很容易看到顶盖移动了，整个躯干也受到了影响。
# **自定义剪切底部**
Aspose.3D for Java允许定制圆柱体的剪切底部。为了使用此功能，您可以使用`Cylinder`类的`setShearBottom()`属性。下面的代码片段显示了如何自定义剪切底部:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

![todo: 图像_alt_文本](working-with-cylinder_2.png)

左圆柱体具有剪切底部到 (0，0.83)，而右圆柱体是序数圆柱体。
# **创建风扇气缸**
Aspose.3D for Java允许创建风扇气缸。为了使用此功能，您可以`setGenerateFanCylinder()` `Cylinder`类的属性来`true`。下面的代码片段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

![todo: 图像_alt_文本](working-with-cylinder_3.png)

左圆柱体具有GenerateFanCylinder = false，右圆柱体具有GenerateFanCylinder = true。
