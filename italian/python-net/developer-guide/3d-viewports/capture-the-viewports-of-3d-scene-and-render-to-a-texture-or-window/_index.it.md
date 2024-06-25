---
title: Cattura le visualizzazioni della scena 3D e rendita a una texture o finestra
type: docs
weight: 20
url: /it/python-net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: Ogni scena 3D può comprendere un numero qualsiasi di visualizzazioni. Utilizzando Aspose.3D for Python via .NET API, gli sviluppatori possono acquisire una o più visualizzazioni in un singolo screenshot. Possono renderizzarlo nell'applicazione .NET basata sulla GUI o in un'immagine.
---
{{% alert color="primary" %}}

Ogni scena 3D può comprendere un numero qualsiasi di visualizzazioni. Utilizzando [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), gli sviluppatori possono acquisire una o più visualizzazioni in un singolo screenshot. Possono renderizzarlo nell'applicazione .NET o in un'immagine basata sulla GUI.

{{% /alert %}}
##  **Catturare e rendering le visualizzazioni della scena 3D**
I metodi `create_render_texture` e `create_render_window` esposti dalla classe [`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory) possono essere utilizzati per creare un nuovo target di rendering che rende la scena una texture o una finestra.
###  **Campione di programmazione**
Questo esempio di codice acquisisce una viewport di 3D scena e la rende in due modi diversi.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-CaptureViewPort-CaptureViewPort.py" >}}
