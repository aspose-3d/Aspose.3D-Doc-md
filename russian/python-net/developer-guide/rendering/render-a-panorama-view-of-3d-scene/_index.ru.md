---
title: Рендеринг панорамного вида сцены 3D
type: docs
weight: 60
url: /ru/python-net/render-a-panorama-view-of-3d-scene/
description: Используя Aspose.3D for Python via .NET API, разработчики могут визуализировать панораму сцены 3D и сохранить этот вид в поддерживаемых форматах изображений.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for Python via .NET API](https:#products.aspose.com/3d/python-net/), разработчики могут отобразить панораму сцены 3D и сохранить этот вид в поддерживаемых форматах изображений.

{{% /alert %}}
##  **Создать вид Panorama**
В этой статье мы создадим камеру и два объекта Light для захвата сцены, также создадим мишень рендеринга, создадим видовой экран и выполним эквипрямоугольную постобработку проекции с картой куба в качестве входных данных и, наконец, сохраним текстуру Panorama. Метод `execute` класса `Renderer` позволяет выполнить эффект пост-обработки и сохранить результат для рендеринга цели.
###  **Образец программирования**
Этот пример кода отображает панораму сцены 3D и сохраняет ее в формате изображения.

**Python**

```py

from aspose.pydrawing.imaging import ImageFormat
from aspose.pydrawing import Color
import aspose.threed as a3d

#load the scene

scene = Scene.from_file("vc.glb")

#create a camera for capturing the cube map

cam = a3d.entities.Camera(a3d.entities.ProjectionType.PERSPECTIVE)


cam.near_plane = 0.1
cam.far_plane = 200
cam.rotation_mode = a3d.entities.RotationMode.FIXED_DIRECTION


scene.root_node.create_child_node(cam).transform.set_translation(5, 6, 0);



#create two lights to illuminate the scene

scene.root_node.create_child_node(a3d.entities.Light("", a3d.entities.LightType.POINT).transform.set_translation(-10, 7, -10)

light = a3d.entities.Light()
light.color = Color.cadet_blue
scene.root_node.create_child_node(light).transform.set_translation(49, 0, 49)

#create a renderer

with a3d.render.Renderer.create_renderer() as renderer:

    #Create a cube map render target with depth texture, depth is required when rendering a scene.

    rt = renderer.render_factory.create_cube_render_texture(a3d.render.RenderParameters(False), 512, 512)

    #create a 2D texture render target with no depth texture used for image processing

    final = renderer.render_factory.CreateRenderTexture(a3d.render.RenderParameters(False, 32, 0, 0), 1024 * 3 , 1024)



    #a viewport is required on the render target

    rt.create_viewport(cam, a3d.utilities.RelativeRectangle.from_scale(0, 0, 1, 1))

    renderer.render(rt)



    #execute the equirectangular projection post-processing with the previous rendered cube map as input

    equirectangular = renderer.get_post_processing("equirectangular")

    #Specify the cube map rendered from the scene as this post processing's input

    equirectangular.input = rt.targets[0]

    #Execute the post processing effect and save the result to render target final

    renderer.execute(equirectangular, final)

    #save the texture into disk

    final.targets[0].save("panorama.png", ImageFormat.PNG)


```
