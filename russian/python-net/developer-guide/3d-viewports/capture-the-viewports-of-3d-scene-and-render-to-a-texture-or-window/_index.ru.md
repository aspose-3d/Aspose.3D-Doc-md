---
title: Захват видовых экранов сцены 3D и рендеринг в текстуру или окно
type: docs
weight: 20
url: /ru/python-net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: Каждая сцена 3D может содержать любое количество видовых экранов. Используя Aspose.3D for Python via .NET API, разработчики могут захватить один или несколько видовых экранов на одном скриншоте. Они могут отобразить его в GUI-приложении .NET или образе.
---
{{% alert color="primary" %}}

Каждая сцена 3D может содержать любое количество видовых экранов. Используя [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), разработчики могут захватить один или несколько видовых экранов на одном скриншоте. Они могут отображать его в GUI-приложении .NET или изображении.

{{% /alert %}}
##  **Захват и рендеринг видовых экранов сцены 3D**
Методы `create_render_texture` и `create_render_window`, выставленные классом [`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory), могут быть использованы для создания новой цели рендеринга, которая визуализирует сцену в текстуре или окне.
###  **Образец программирования**
Этот пример кода захватывает видовой экран 3D Scene и отображает его двумя различными способами.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-CaptureViewPort-CaptureViewPort.py" >}}
