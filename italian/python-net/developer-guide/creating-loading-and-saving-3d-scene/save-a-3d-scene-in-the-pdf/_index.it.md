---
title: Salva una scena di 3D in PDF
type: docs
weight: 60
url: /it/python-net/save-a-3d-scene-in-the-pdf/
description: La classe Scena di Aspose.3D API rappresenta una scena di 3D. Gli sviluppatori possono creare una scena da 3D aggiungendo fotocamera, luce, poligoni e varie altre entità. Ora possono anche salvare una scena di 3D nel formato di file PDF.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) di Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono creare una scena da 3D aggiungendo fotocamera, luce, poligoni e varie altre entità. Ora possono anche salvare una scena di 3D nel formato di file PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for Python via .NET scrive direttamente le informazioni relative a API e al numero di versione nei documenti di output. Ad esempio, quando si esegue il rendering di un disegno a PDF, Aspose.3D for Python via .NET popolano il campo `Application` con valore 'Aspose. Campo 3D 'e `PDF Producer` con valore, e.g' Aspose.3D 17,9 '.

Tieni presente che non puoi istruire Aspose. Diagramma per Python via .NET API per modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}} 
##  **Crea 3D PDF con un cilindro e renderizzato in modalità illustrazione ombreggiata con illuminazione ottimizzata CAD**
Il metodo Salva della classe `Scene` consente di salvare una scena 3D nel formato PDF. Gli sviluppatori possono caricare qualsiasi file supportato da 3D o creare una nuova scena 3D, possono salvare una scena 3D nel formato PDF come mostrato in questo esempio di codice:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Cylinder
from aspose.threed.shading import PhongMaterial
from aspose.threed.formats import PdfSaveOptions, PdfLightingScheme, PdfRenderMode
# Create a new scene
scene = Scene()
# Create a cylinder child node
cylinder = scene.root_node.create_child_node("cylinder", Cylinder())
cylinder.material = PhongMaterial()
# Set rendering mode and lighting scheme
opt = PdfSaveOptions()
opt.lighting_scheme = PdfLightingScheme.CAD
opt.render_mode = PdfRenderMode.SHADED_ILLUSTRATION
# Save in the PDF format
scene.save("output_out.pdf", opt)

{{< /highlight >}}
