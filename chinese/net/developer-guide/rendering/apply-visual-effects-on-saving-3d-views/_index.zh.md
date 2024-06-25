---
title: 在保存 3D 个视图时应用视觉效果
type: docs
weight: 10
url: /zh/net/apply-visual-effects-on-saving-3d-views/
description: 使用 Aspose.3D for .NET API，开发人员可以在保存到图像之前对 3D 视图应用视觉效果。这些视觉效果也称为后处理效果或滤镜，它们实时应用于 3D 视图中显示的所有内容。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET API](https://products.aspose.com/3d/net/)，开发人员可以在保存到图像之前对 3D 视图应用视觉效果。这些视觉效果也称为后处理效果或过滤器，它们实时应用于 3D 视图中显示的所有内容。

{{% /alert %}}
##  **在 3D 视图上应用视觉效果**
[`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) 类的 [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) 方法允许创建任何受支持的视觉效果。Renderer类提供了一个 [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) 成员来应用各种过滤器，PostProcessings类的Add方法允许在呈现之前合并一个过滤器。
###  **编程示例**
此代码示例对 3D 视图应用视觉效果。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
