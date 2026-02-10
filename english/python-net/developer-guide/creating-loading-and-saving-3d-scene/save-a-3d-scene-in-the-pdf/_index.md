---
title: Save a 3D Scene in the PDF
type: docs
weight: 60
url: /python-net/save-a-3d-scene-in-the-pdf/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can build a 3D scene by adding Camera, Light, polygons and various other entities. They can also now save a 3D scene in the PDF file format.
---

{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can build a 3D scene by adding Camera, Light, polygons and various other entities. They can also now save a 3D scene in the PDF file format.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for Python via .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.3D for Python via .NET populates `Application` field with value 'Aspose.3D' and `PDF Producer` field with value, e.g 'Aspose.3D 17.9'.

Please note that you cannot instruct Aspose.Diagram for Python via .NET API to change or remove this information from output Documents.

{{% /alert %}} 
## **Create a 3D PDF with a Cylinder, and Rendered in Shaded Illustration Mode with CAD Optimized Lighting**
The Save method of the `Scene` class allows to save a 3D scene in the PDF format. Developers may load any 3D supported file or build a new 3D scene, they can save a 3D scene in the PDF format as shown in this code example:

{{< highlight "python" >}}
from aspose.pydrawing import Color
from aspose.threed import Scene
from aspose.threed.entities import Cylinder
from aspose.threed.formats import PdfLightingScheme, PdfRenderMode, PdfSaveOptions
from aspose.threed.shading import PhongMaterial
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a new scene
scene = Scene()
material = PhongMaterial()
material.diffuse_color = Vector3(Color.dark_cyan)
#  Create a cylinder child node
scene.root_node.create_child_node("cylinder", Cylinder()).material = material
#  Set rendering mode and lighting scheme
opt = PdfSaveOptions()
opt.lighting_scheme = PdfLightingScheme.CAD
opt.render_mode = PdfRenderMode.SHADED_ILLUSTRATION
#  Save in the PDF format
scene.save("out"  + "output_out.pdf", opt)
{{< /highlight >}}
