---
title: Working مع Radius من Sphere
type: docs
weight: 110
url: /ar/python-net/working-with-radius-of-sphere/
description: باستخدام Aspose.3D for Python via .NET ، يمكنك تعيين الحصول على نصف قطر كروي. من أجل الحصول على أو ضبط نصف القطر ، يمكنك استخدام خاصية نصف القطر لفئة كروية. فيما يلي عينة الكود لتعيين نصف قطر كروي.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.4 أو أكبر.

{{% /alert %}} 
##  **Work مع Radius من Sphere**
باستخدام Aspose.3D for Python via .NET ، يمكنك تعيين الحصول على نصف قطر كروي. للحصول على نصف قطر أو ضبطه ، يمكنك استخدام خاصية `radius` من فئة `Sphere`. فيما يلي عينة الكود لتعيين نصف قطر كروي.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
sphere = Sphere()
sphere.radius = 10 .0
#  Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.root_node.create_child_node(sphere)
#  Save scene
scene.save("data-dir"  + "sphere.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
