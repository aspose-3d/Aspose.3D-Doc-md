---
title: Capture the Viewports of 3D Scene and Render to a Texture or Window
type: docs
weight: 20
url: /python-net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: Each 3D scene can comprise of any number of viewports. Using Aspose.3D for Python via .NET API, developers can capture one or more viewports in a single screenshot. They may render it in the GUI based .NET application or an image.
---

{{% alert color="primary" %}}

Each 3D scene can comprise of any number of viewports. Using [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), developers can capture one or more viewports in a single screenshot. They may render it in the GUI based .NET application or an image.

{{% /alert %}}
## **Capturing and Rendering the Viewports of 3D Scene**
The `create_render_texture` and `create_render_window` methods exposed by the [`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory) class can be used to create a new render target that renders the scene to a texture or Window.
### **Programming Sample**
This code example captures a viewport of 3D Scene and renders it in two different ways.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-CaptureViewPort-CaptureViewPort.py" >}}
