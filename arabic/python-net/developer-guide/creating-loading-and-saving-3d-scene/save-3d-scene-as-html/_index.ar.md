---
title: وفِّر 3D مشهد بـ HTML
type: docs
weight: 90
url: /ar/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.9 أو أكبر.

{{% /alert %}} 
#  **وفِّر 3D مشهد بـ HTML**
Aspose.3D for Python via .NET provides `Html5SaveOptions` class to save a save 3D scene as HTML. When you export the scene into HTML5 file, API will export three files, an `HTML` file, an Aspose3DWeb file(*.*a3dw**), and a rendered `JavaScript` file. In order to export a3dw file only, you can specify Aspose3DWeb as the export type, and reuse the JavaScript file within your own HTML page. The following code snippet shows how to save a 3D scene as HTML. 



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

نظرًا لحدود أمان المتصفح ، لا يمكن فتح ملف HTML الذي تم تصديره مباشرة ، تحتاج إلى فتحه من خلال خادم ويب ، إذا كان لديك تثبيت python3 ، يمكنك بدء تشغيل خادم الويب في سطر الأوامر في الدليل الذي تم تصديره

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Tالدجاجة فتحه<http://localhost:8000/test.html>. The يستخدم بائع الويب ebebGL2 ، يمكنك استخدام<https://get.webgl.org/webgl2/>للتحقق مما إذا كان المتصفح يدعم ذلك أم لا.


