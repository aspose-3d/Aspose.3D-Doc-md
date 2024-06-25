---
title: Capturar las ventanas de la escena 3D y render a una textura o ventana
type: docs
weight: 20
url: /es/net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: Cada escena 3D puede comprender cualquier número de ventanas gráficas. Con Aspose.3D for .NET API, los desarrolladores pueden capturar una o más ventanas gráficas en una sola captura de pantalla. Pueden renderizarlo en la aplicación .NET basada en la GUI o en una imagen.
---
{{% alert color="primary" %}}

Cada escena 3D puede comprender cualquier número de ventanas gráficas. Usando [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), los desarrolladores pueden capturar una o más ventanas gráficas en una sola captura de pantalla. Pueden renderizarlo en la aplicación .NET basada en GUI o en una imagen.

{{% /alert %}}
##  **Capturar y renderizar los viewports de la escena 3D**
Los métodos `CreateRenderTexture` y `CreateRenderWindow` expuestos por la clase [`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory) se pueden utilizar para crear un nuevo destino de renderizado que renderiza la escena en una textura o ventana.
###  **Muestra de programación**
Este ejemplo de código captura una ventana gráfica de 3D Scene y la representa de dos maneras diferentes.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-CaptureViewPort-CaptureViewPort.cs" >}}
