---
title: 将 3D 场景另存为 HTML
type: docs
weight: 90
url: /zh/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

19.9或更高版本支持此功能。

{{% /alert %}} 
#  **将 3D 场景另存为 HTML**
Aspose.3D for Python via .NET 提供 `Html5SaveOptions` 类以将 3D 场景另存为 HTML。将场景导出到 HTML5 文件时，API 将导出三个文件: 一个 `HTML` 文件、一个 Aspose 3dweb文件 (*.* a3dw **) 和一个渲染的 `JavaScript` 文件。为了只导出a3dw文件，您可以指定 Aspose 3dweb作为导出类型，并在您自己的 HTML 页面中重用JavaScript文件。下面的代码片段显示了如何将 3D 场景保存为 HTML。



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

由于浏览器的安全限制，导出的 HTML 文件不能直接打开，您需要通过web服务器打开它，如果您安装了python3，您可以在导出目录中的命令行中启动web服务器

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

然后打开它<http://localhost:8000/test.html>。web渲染器使用WebGL2，您可以使用<https://get.webgl.org/webgl2/>检查您的浏览器是否支持它。


