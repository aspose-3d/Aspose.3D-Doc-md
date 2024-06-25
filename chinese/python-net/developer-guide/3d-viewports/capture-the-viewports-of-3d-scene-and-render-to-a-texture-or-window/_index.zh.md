---
title: 捕获 3D 场景的视口并渲染到纹理或窗口
type: docs
weight: 20
url: /zh/python-net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: 每个 3D 场景可以包含任意数量的视口。使用 Aspose.3D for Python via .NET API，开发人员可以在单个屏幕截图中捕获一个或多个视口。他们可以在基于GUI的 .NET 应用程序或图像中呈现它。
---
{{% alert color="primary" %}}

每个 3D 场景可以包含任意数量的视口。使用 [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/)，开发人员可以在单个屏幕截图中捕获一个或多个视口。他们可以在基于GUI的 .NET 应用程序或图像中呈现它。

{{% /alert %}}
##  **捕获和渲染 3D 场景的视口**
[`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory) 类公开的 `create_render_texture` 和 `create_render_window` 方法可用于创建将场景渲染到纹理或窗口的新渲染目标。
###  **编程示例**
此代码示例捕获 3D 场景的视口，并以两种不同的方式呈现它。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-CaptureViewPort-CaptureViewPort.py" >}}
