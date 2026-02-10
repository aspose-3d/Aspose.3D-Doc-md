---
title: تقديم عرض 3D بتنسيق صورة من الكاميرا
type: docs
weight: 50
url: /ar/python-net/render-3d-view-in-image-format-from-camera/
description: باستخدام Aspose.3D for Python via .NET ، يمكن للمطورين عرض صورة لعرض صورة واقعية لطراز 3D ، مع أو بدون الخلفية المحسنة ، والقوام ، والظلال ، وكذلك ضبط حجم الصورة.
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) ، يمكن للمطورين عرض صورة لعرض صورة واقعية لطراز 3D ، مع أو بدون الخلفية المحسنة ، والقوام ، والظلال ، وكذلك ضبط حجم الصورة.

{{% /alert %}}
##  **التقط صورة لطراز 3D من الكاميرا**
يمكن استخدام طريقة تقديم العرض التي تعرضها فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) لالتقاط صورة من الكاميرا النشطة. يمكن للمطورين أيضًا استخدام عدة طرق مختلفة للتنقل ووضع الكاميرا في المشهد. في هذا المثال البرمجي ، نقوم بإنشاء كاميرا في الموضع (10,10,10) في مشهد 3D موجود وننظر إلى نقطة الأصل للعرض.
###  **Pروغرامينغ ple وافرة**
يُنشئ مثال الرمز هذا كاميرا في مشهد 3D ، ويُحدد هدفها ويُعرض صورة.

{{< highlight "python" >}}
from aspose.pydrawing import Color, Size
from aspose.pydrawing.imaging import ImageFormat
from aspose.threed import ImageRenderOptions, Scene
from aspose.threed.entities import Camera
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load scene from file
scene = Scene("data-dir"  + "camera.3ds")
#  Create a camera at (10,10,10) and look at the origin point for rendering,
#  It must be attached to the scene before render
camera = Camera()
scene.root_node.create_child_node("camera", camera)
camera.parent_node.transform.translation = Vector3(10, 10, 10)
camera.look_at = Vector3.ORIGIN
#  Specify the image render option
opt = ImageRenderOptions()
#  Set the background color
opt.background_color = Color.alice_blue
#  Tells renderer where the it can find textures
opt.asset_directories.append("data-dir"  + "textures")
#  Turn on shadow
opt.enable_shadows = True
#  Render the scene in given camera's perspective into specified png file with size 1024x1024
scene.render(camera, "out"  + "Render3DModelImageFromCamera.png", Size(1024, 1024), ImageFormat.png, opt)

{{< /highlight >}}
