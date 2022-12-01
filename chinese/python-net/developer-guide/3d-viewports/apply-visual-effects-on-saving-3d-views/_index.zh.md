---
title: 在保存3D视图上应用视觉效果
type: docs
weight: 10
url: /zh/python-net/apply-visual-effects-on-saving-3d-views/
description: 使用Aspose.3D进行Python via .NET API，开发人员可以在保存图像之前对3D视图应用视觉效果。这些视觉效果也被称为实时应用于3D视图中显示的所有内容的后处理效果或过滤器。
---
{{% alert color="primary" %}}

使用[Aspose.3D Python via .NET API](https://products.aspose.com/3d/python-net/),开发人员可以在保存图像之前对3D视图应用视觉效果。这些视觉效果也被称为实时应用于3D视图中显示的所有内容的后处理效果或过滤器。

{{% /alert %}}
## **在3D视图上应用视觉效果**
[`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer)类的[`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing)方法允许创建任何受支持的视觉效果。`Renderer`类提供[`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings)成员来应用各种过滤器，`PostProcessings`类的Add方法允许在渲染之前合并过滤器。
### **编程示例**
此代码示例在3D视图上应用视觉效果。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
