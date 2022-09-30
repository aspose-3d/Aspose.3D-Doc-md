---
title: Applicare effetti visivi sul risparmio di visualizzazioni 3D
type: docs
weight: 10
url: /it/python-net/apply-visual-effects-on-saving-3d-views/
description: Utilizzando Aspose.3D per Python via .NET API, gli sviluppatori possono applicare effetti visivi su 3D Views prima di salvare nell'immagine. Questi effetti visivi sono noti anche come effetti o filtri post-elaborazione che vengono applicati in tempo reale a tutto ciò che viene visualizzato nella visualizzazione 3D.
---
{{% alert color="primary" %}}

Utilizzo[Aspose.3D per Python via .NET API](https://products.aspose.com/3d/python-net/), Gli sviluppatori possono applicare effetti visivi su 3D Views prima di salvare nell'immagine. Questi effetti visivi sono noti anche come effetti o filtri post-elaborazione che vengono applicati in tempo reale a tutto ciò che viene visualizzato nella visualizzazione 3D.

{{% /alert %}}
## **Applicare gli effetti visivi sulla vista 3D**
Il metodo [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) della classe [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) consente di creare qualsiasi effetto visivo supportato. La classe `Renderer` offre un membro [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) per applicare vari filtri, il metodo Aggiungi della classe `PostProcessings` consente di incorporare un filtro prima del rendering.
### **Campione di programmazione**
Questo esempio di codice applica l'effetto visivo su una vista 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
