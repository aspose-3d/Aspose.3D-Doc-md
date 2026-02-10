---
title: Guardar una escena 3D en el PDF
type: docs
weight: 60
url: /es/python-net/save-a-3d-scene-in-the-pdf/
description: La clase Scene de Aspose.3D API representa una escena 3D. Los desarrolladores pueden construir una escena 3D añadiendo cámara, luz, polígonos y varias otras entidades. Ahora también pueden guardar una escena 3D en el formato de archivo PDF.
---
{{% alert color="primary" %}} 

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la Aspose.3D API representa una escena 3D. Los desarrolladores pueden construir una escena 3D agregando Cámara, Luz, polígonos y varias otras entidades. Ahora también pueden guardar una escena 3D en el formato de archivo PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for Python via .NET escribe directamente la información sobre API y el número de versión en los documentos de salida. Por ejemplo, al representar un dibujo en PDF, Aspose.3D for Python via .NET rellena el campo `Application` con el valor 'Aspose.3D' y `PDF Producer` campo con valor, e.g 'Aspose.3D 17,9'.

Tenga en cuenta que no puede indicar a Aspose. Diagrama de Python via .NET API para cambiar o quitar esta información de documentos de salida.

{{% /alert %}} 
##  **Cree un 3D PDF con un cilindro y renderizado en modo de ilustración sombreada con CAD Iluminación optimizada**
El método Save de la clase `Scene` permite guardar una escena 3D en el formato PDF. Los desarrolladores pueden cargar cualquier archivo compatible con 3D o construir una nueva escena 3D, pueden guardar una escena 3D en el formato PDF como se muestra en este ejemplo de código:

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
