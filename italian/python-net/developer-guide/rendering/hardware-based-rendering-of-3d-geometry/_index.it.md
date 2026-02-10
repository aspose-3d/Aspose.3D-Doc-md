---
title: Rendering basato su hardware di 3D geometria
type: docs
weight: 30
url: /it/python-net/hardware-based-rendering-of-3d-geometry/
description: Utilizzando Aspose.3D for Python via .NET API, gli sviluppatori possono programmare la GPU (unità di elaborazione grafica) e configurare l'hardware grafico per il rendering della geometria 3D invece della pipeline di funzioni fisse.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, gli sviluppatori possono programmare la GPU (unità di elaborazione grafica) e configurare l'hardware grafico per il rendering della geometria 3D invece della pipeline di funzioni fisse. In questo articolo, ci concentriamo sul rendering basato su hardware utilizzando [OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirettX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirettX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) e [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Crea hardware e renderizza una geometria di 3D**
Per rendere una geometria 3D, sono necessari uno shader, buffer e stato di rendering. Nessuno di loro può lavorare l'uno senza l'altro.

- **Tamponi**-Gli elenchi dei triangoli sono triangoli individuali specificati in un array a volte indicato come buffer. In un elenco di triangolo, ogni triangolo viene specificato individualmente. I punti di un triangolo possono essere condivisi utilizzando gli indici per ridurre la quantità di dati che devono essere passati all'hardware grafico.
- **Ombanti**-Definisce come trasformare i triangoli dallo spazio mondiale nello spazio dello schermo e calcolare il colore del pixel finale sul lato GPU
- **Stati di rendita**-Fornisce parametri per la GPU per rasterizzare i triangoli in pixel.

{{% alert color="primary" %}}

Abbiamo preparato un progetto demo. Fai riferimento a [Questo URL di download](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

OpenGL Shading Language (GLSL) è il linguaggio di ombreggiatura standard di alto livello per la grafica OpenGL API. Esistono tre tipi di shader comunemente usati: Vertex Shader, Frammento Shader e Geometry Shaders.

La classe [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) dice al renderer, il codice sorgente è per il linguaggio di ombreggiatura OpenGL, può essere compilato in [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram) classe. La classe [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) definisce le variabili utilizzate nello shader. La classe `VariableSemantic` viene utilizzata per identificare la semantica della variabile shader, Aspose. Il renderer 3D preparerà automaticamente i valori delle variabili shader a seconda della semantica.
###  **Campione di programmazione per Shader**
Questo esempio di codice inizializza renderer e Shader per la griglia. Puoi scaricare il progetto di lavoro completo di questo esempio da [Qui](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
###  **Campione di programmazione per il buffer e lo stato di rendering**
Questo esempio di codice inizializza il buffer e lo stato di rendering per la griglia.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
