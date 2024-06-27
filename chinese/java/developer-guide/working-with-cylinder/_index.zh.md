---
title: 与气缸一起工作
type: docs
weight: 100
url: /zh/java/working-with-cylinder/
description: Aspose.3D for Java 允许自定义圆柱体的偏移顶部。为了使用此功能，您可以使用Cylinder类的setOffsetTop() 方法。
---
#  **自定义偏移顶部**
Aspose.3D for Java 允许自定义圆柱体的偏移顶部。为了使用此功能，您可以使用 `Cylinder` 类的 `setOffsetTop()` 方法。以下代码段显示了如何自定义偏移顶部:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

![todo: 图像 _ alt_text](working-with-cylinder_1.png)

左边的OffsetTop设置为 (5,3，0)，很容易看到顶盖移动了，整个躯干也受到了影响。
#  **自定义剪切底部**
Aspose.3D for Java 允许自定义圆柱体的剪切底部。为了使用此功能，您可以使用 `Cylinder` 类的 `setShearBottom()` 属性。以下代码段显示了如何自定义剪切底部:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

![todo: 图像 _ alt_text](working-with-cylinder_2.png)

左圆柱体具有剪切底部到 (0，0.83)，而右圆柱体是序数圆柱体。
#  **创建风扇气缸**
Aspose.3D for Java 允许创建风扇圆柱体。为了使用此功能，您可以将 `Cylinder` 类的 `setGenerateFanCylinder()` 属性设置为 `true`。以下代码段显示了如何使用此功能:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

![todo: 图像 _ alt_text](working-with-cylinder_3.png)

左圆柱体具有GenerateFanCylinder = false，右圆柱体具有GenerateFanCylinder = true。
