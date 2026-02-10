---
title: Guardar 3D Escena como HTML
type: docs
weight: 90
url: /es/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,9 o superior.

{{% /alert %}} 
#  **Guardar 3D Escena como HTML**
Aspose.3D for Python via .NET proporciona la clase `Html5SaveOptions` para guardar una escena de 3D como HTML. Cuando exporte la escena a un archivo HTML5, API exportará tres archivos, un archivo `HTML`, un archivo Aspose3DWeb (*.* a3dw **) y un archivo `JavaScript` representado. Para exportar solo el archivo a3dw, puede especificar Aspose3DWeb como el tipo de exportación y reutilizar el archivo JavaScript dentro de su propia página HTML. El siguiente fragmento de código muestra cómo guardar una escena 3D como HTML.



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

Debido a los límites de seguridad del navegador, el archivo HTML exportado no se puede abrir directamente, debe abrirlo a través de un servidor web, si tiene python3 instalado, puede iniciar el servidor web en la línea de comandos en el directorio exportado

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Entonces ábrelo<http://localhost:8000/test.html>... El renderizador web utiliza WebGL2, usted puede utilizar<https://get.webgl.org/webgl2/>Para comprobar si su navegador es compatible o no.


