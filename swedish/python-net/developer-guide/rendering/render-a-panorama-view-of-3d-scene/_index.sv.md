---
title: Rendera en Panorama vy av 3D scena
type: docs
weight: 60
url: /sv/python-net/render-a-panorama-view-of-3d-scene/
description: Med Aspose.3D för Python via .NET API, utvecklare kan ge en panoramavy av 3D scen och spara den vyn i de bildformat som stöds.
---
{{% alert color="primary" %}}

Användning[Aspose.3D för Python via .NET API](https:#products.aspose.com/3d/python-net/), Kan utvecklare återge en panoramavy av 3D scen och spara den vyn i de bildformat som stöds.

{{% /alert %}}
## **Skapa en panoramavy**
I den här artikeln skapar vi en kamera och två Ljus objekt för att fånga scenen, också skapa en rendering mål, skapa en visningsport och kör den ekvattangulära projektionen efterbehandling med kubenkartan som inmatning och slutligen spara Panen Orama konsistens. `execute`-metoden `Renderer`-klass gör det möjligt att utföra efterbehandlingseffekten och spara resultatet för att göra mål.
### **Programmeringsprova**
Detta kodexempel ger en Panorama vy av 3D scen och spara i bildformatet.

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
