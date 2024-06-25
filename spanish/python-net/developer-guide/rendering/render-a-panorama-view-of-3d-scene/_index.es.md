---
title: Render una vista panorámica de la escena 3D
type: docs
weight: 60
url: /es/python-net/render-a-panorama-view-of-3d-scene/
description: Con Aspose.3D for Python via .NET API, los desarrolladores pueden representar una vista panorámica de la escena 3D y guardar esa vista en los formatos de imagen compatibles.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for Python via .NET API](https:#products.aspose.com/3d/python-net/), los desarrolladores pueden representar una vista panorámica de la escena 3D y guardar esa vista en los formatos de imagen compatibles.

{{% /alert %}}
##  **Crear una vista panorámica**
En este artículo, creamos una cámara y dos objetos de luz para capturar la escena, también creamos un destino de render, creamos una ventana gráfica y ejecutamos el post-procesamiento de proyección equirectangular con el mapa de cubo como entrada y, finalmente, guardamos la textura Panorama. El método `execute` de la clase `Renderer` permite ejecutar el efecto posterior al procesamiento y guardar el resultado para representar el destino.
###  **Muestra de programación**
Este ejemplo de código representa una vista panorámica de la escena 3D y la guarda en el formato de imagen.

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
