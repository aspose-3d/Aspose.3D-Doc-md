---
title: Risparmia 3D Scena come HTML
type: docs
weight: 90
url: /it/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.9 o maggiore.

{{% /alert %}} 
#  **Risparmia 3D Scena come HTML**
Aspose.3D for Python via .NET offre una classe `Html5SaveOptions` per salvare una scena di 3D di risparmio come HTML. Quando esporti la scena in file HTML5, API esporterà tre file, un file `HTML`, un file DWeb Aspose3 (*.* a3dw **) e un file `JavaScript` reso. Per esportare solo file a3dw, è possibile specificare Aspose3DWeb come tipo di esportazione e riutilizzare il file JavaScript all'interno della propria pagina HTML. Il seguente frammento di codice mostra come salvare una scena di 3D come HTML.



{{< highlight "python" >}}
from aspose.pydrawing import Color
from aspose.threed import Scene
from aspose.threed.entities import Cylinder, Light, LightType
from aspose.threed.formats import Html5SaveOptions
from aspose.threed.shading import LambertMaterial
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize 3D scene
scene = Scene()
#  Create a child node
node = scene.root_node.create_child_node(Cylinder())
material = LambertMaterial()
material.diffuse_color = Vector3(Color.chartreuse)
#  Set child node properites
node.material = material
light = Light()
light.light_type = LightType.POINT
scene.root_node.create_child_node(light).transform.translation = Vector3(10, 0, 10)
#  Create a Html5SaveOptions
opt = Html5SaveOptions()
# Turn off the grid
opt.show_grid = False
# Turn off the user interface
opt.show_ui = False
#  Save 3D to HTML5
scene.save("data-dir"  + "D:\\HtmlSaveOption.html", opt)

{{< /highlight >}}

{{% alert color="primary" %}} 

A causa dei limiti di sicurezza del browser, il file HTML esportato non può essere aperto direttamente, è necessario aprirlo tramite un server Web, se è installato python3, è possibile avviare il server Web nella riga di comando nella directory esportata

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Allora aprilo<http://localhost:8000/test.html>. Il renderer web utilizza WebGL2, è possibile utilizzare<https://get.webgl.org/webgl2/>Per verificare se il tuo browser lo supporta o meno.


