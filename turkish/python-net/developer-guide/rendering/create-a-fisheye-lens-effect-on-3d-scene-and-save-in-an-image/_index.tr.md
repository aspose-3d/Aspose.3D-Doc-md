---
title: 3D sahnesinde balık gözü lens efekti oluşturun ve bir görüntüde kaydedin
type: docs
weight: 20
url: /tr/python-net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/
description: Aspose.3D for Python via .NET API kullanarak, geliştiriciler 3D sahnesinde balıkgözü lens etkisi oluşturabilir ve bu görünümü desteklenen görüntü formatlarına kaydedebilir.
---
{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET API](https:#products.aspose.com/3d/python-net/), developers can create a Fisheye lens effect on 3D scene and save that view into the supported image formats.

{{% /alert %}}
##  **Create bir Fisheye lens etkisi**
Bu makalede, sahneyi yakalamak için bir kamera ve iki ışık nesnesi oluşturuyoruz, aynı zamanda bir render hedefi oluşturuyoruz, bir bakış açısı oluşturuyoruz ve küp haritasıyla balık gözü projeksiyon işlemini giriş olarak gerçekleştiriyoruz ve sonunda balık gözü dokusunu kaydediyoruz. `execute` `Renderer` sınıfı yöntemi, posta işleme etkisini çalıştırmayı ve hedefi işlemek için sonucu kaydetmeyi sağlar.
###  **Programming ample ample**
Bu kod örneği, 3D sahnesinde balıkgözü lens etkisi yaratır ve görüntü formatına kaydeder.

**Python**


```py

import aspose.threed as a3d
from aspose.pydrawing import Color
from aspose.pydrawing.imaging import ImageFormat

#load the scene

scene = a3d.Scene.from_file("test.glb");

#create a camera for capturing the cube map

cam = a3d.entities.Camera(a3d.entities.ProjectionType.PERSPECTIVE)

cam.near_plane = 0.1
cam.far_plane = 200
cam.rotation_mode = a3d.entities.RotationMode.FIXED_DIRECTION

scene.root_node.create_child_node(cam).transform.set_translation(5, 6, 0)



#create two lights to illuminate the scene

light = a3d.entities.Light()
light.light_type = a3d.entities.LightType.POINT

scene.root_node.create_child_node(light).transform.set_translation(-10, 7, -10)


light = a3d.entities.Light()
light.color = a3d.utilities.Vector3(Color.cadet_blue)


scene.root_node.create_child_node(light).transform.set_translation(49, 0, 49)


#create a renderer

with a3d.render.Renderer.create_renderer() as renderer:

    #Create a cube map render target with depth texture, depth is required when rendering a scene.
    rt = renderer.render_factory.create_cube_render_texture(a3d.render.RenderParameters(False), 512, 512)

    #create a 2D texture render target with no depth texture used for image processing
    final = renderer.rendere_factory.create_render_texture(a3d.render.RenderParameters(False, 32, 0, 0), 1024, 1024)



    #a viewport is required on the render target
    rt.create_viewport(cam, RelativeRectangle.from_scale(0, 0, 1, 1))

    renderer.render(rt)


    #execute the fisheye projection post-processing with the previous rendered cube map as input
    #the fisheye can have field of view more than 180 degree, so a cube map with all direction is required.

    fisheye = renderer.get_post_processing("fisheye")

    # we can change the fov to 360 instead of the default value 180.

    fisheye.find_property("fov").Value = 360.0

    #Specify the cube map rendered from the scene as this post processing's input

    fisheye.input = rt.targets[0]

    #Execute the post processing effect and save the result to render target final

    renderer.execute(fisheye, final)

    #save the texture into disk

    final.targets[0].save("fisheye.png", ImageFormat.PNG)


```
