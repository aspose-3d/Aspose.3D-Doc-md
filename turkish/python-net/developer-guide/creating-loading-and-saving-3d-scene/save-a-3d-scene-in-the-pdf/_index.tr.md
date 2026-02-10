---
title: 3D sahnesinde PDF
type: docs
weight: 60
url: /tr/python-net/save-a-3d-scene-in-the-pdf/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can build a 3D scene by adding Camera, Light, polygons and various other entities. They can also now save a 3D scene in the PDF file format.
---
{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can build a 3D scene by adding Camera, Light, polygons and various other entities. They can also now save a 3D scene in the PDF file format.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for Python via .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.3D for Python via .NET populates `Application` field with value 'Aspose.3D' and `PDF Producer` field with value, e.g 'Aspose.3D 17.9'.

Please note that you cannot instruct Aspose.Diagram for Python via .NET API to change or remove this information from output Documents.

{{% /alert %}} 
##  **Bir silindir ile 3D PDF oluşturun ve CAD optimize edilmiş aydınlatma ile gölgeli illüstrasyon modunda işleyin**
The Save method of the `Scene` class allows to save a 3D scene in the PDF format. Developers may load any 3D supported file or build a new 3D scene, they can save a 3D scene in the PDF format as shown in this code example:

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
