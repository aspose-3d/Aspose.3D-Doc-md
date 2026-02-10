---
title: Sparen Sie 3D Szene als HTML
type: docs
weight: 90
url: /de/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.9 oder höher unterstützt.

{{% /alert %}} 
#  **Sparen Sie 3D Szene als HTML**
Aspose.3D for Python via .NET bietet `Html5SaveOptions` Klasse, um eine Save 3D Szene als HTML zu speichern. Wenn Sie die Szene in HTML5-Datei exportieren, exportieren API drei Dateien, eine `HTML`-Datei, eine Aspose3DWeb-Datei (*.* a3dw **) und eine gerenderte `JavaScript`-Datei. Um nur a3dw-Datei zu exportieren, können Sie Aspose3DWeb als Export typ angeben und die JavaScript-Datei innerhalb Ihrer eigenen HTML-Seite wieder verwenden. Das folgende Code-Snippet zeigt, wie Sie eine 3D-Szene als HTML speichern.



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

Aufgrund der Sicherheits grenzen des Browsers kann die exportierte HTML-Datei nicht direkt geöffnet werden. Sie müssen sie über einen Webserver öffnen. Wenn Sie python3 installiert haben, können Sie den Webserver in der Befehlszeile im exportierten Verzeichnis starten

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Dann öffnen Sie es<http://localhost:8000/test.html>. Der Web-Renderer nutzt WebGL2, Sie können<https://get.webgl.org/webgl2/>Um zu überprüfen, ob Ihr Browser es unterstützt oder nicht.


