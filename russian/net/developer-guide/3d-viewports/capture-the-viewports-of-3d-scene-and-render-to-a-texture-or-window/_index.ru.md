---
title: Захват видовых окон сцены 3D и отправка в текстуру или окно
type: docs
weight: 20
url: /ru/net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: Каждая сцена 3D может содержать любое количество видовых экранов. Используя Aspose.3D for .NET API, разработчики могут захватывать один или несколько видовых экранов на одном скриншоте. Они могут визуализировать его в приложении .NET на основе GUI или в изображении.
---
{{% alert color="primary" %}}

Каждая сцена 3D может содержать любое количество видовых экранов. Используя[Aspose.3D for .NET 0761234881](https://products.aspose.com/3d/net/), Разработчики могут захватывать один или несколько видовых экранов на одном скриншоте. Они могут визуализировать его в приложении .NET на основе GUI или в изображении.

{{% /alert %}}
## **Снятия и Рендеринг видовых окон сцены 3D**
Методы `CreateRenderTexture` и `CreateRenderWindow`, открытые классом [`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory), могут быть использованы для создания новой цели рендеринга, которая отображает сцену в текстуру или окно.
### **Образец программирования**
В этом примере кода фиксируется видовой экран сцены 3D и визуализирует его двумя разными способами.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-CaptureViewPort-CaptureViewPort.cs" >}}
