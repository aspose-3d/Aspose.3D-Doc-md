---
title: 在保存3D视图上应用视觉效果
type: docs
weight: 10
url: /zh/net/apply-visual-effects-on-saving-3d-views/
description: 使用Aspose.3D for .NET API，开发人员可以在保存图像之前对3D视图应用视觉效果。这些视觉效果也被称为实时应用于3D视图中显示的所有内容的后处理效果或过滤器。
---
{{% alert color="primary" %}}

使用[Aspose.3D for .NET API](https://products.aspose.com/3d/net/),开发人员可以在保存图像之前对3D视图应用视觉效果。这些视觉效果也被称为实时应用于3D视图中显示的所有内容的后处理效果或过滤器。

{{% /alert %}}
## **在3D视图上应用视觉效果**
[`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer)类的[`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing)方法允许创建任何受支持的视觉效果。渲染器类提供[`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings)成员来应用各种过滤器，postprocessing类的Add方法允许在渲染之前合并过滤器。
### **编程示例**
此代码示例在3D视图上应用视觉效果。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
