---
title: Erstellen Sie eine Panorama ansicht der 3D-Szene
type: docs
weight: 60
url: /de/python-net/render-a-panorama-view-of-3d-scene/
description: Mit Aspose.3D for Python via .NET API können Entwickler eine Panorama ansicht der 3D-Szene rendern und diese Ansicht in den unterstützten Bildformaten speichern.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for Python via .NET API](https:#products.aspose.com/3d/python-net/) können Entwickler eine Panorama ansicht der 3D-Szene rendern und diese Ansicht in den unterstützten Bildformaten speichern.

{{% /alert %}}
##  **Erstellen Sie eine Panorama-Ansicht**
In diesem Artikel erstellen wir eine Kamera und zwei Licht objekte, um die Szene zu erfassen, erstellen auch ein Render ziel, erstellen ein Ansicht fenster und führen die äqui rechteckige Projektions post verarbeitung mit der Würfel karte als Eingabe aus und speichern schließlich die Panorama-Textur. Die `execute`-Methode der `Renderer`-Klasse ermöglicht es, den Nach bearbeitungs effekt auszuführen und das Ergebnis zu speichern, um das Ziel zu rendern.
###  **Programmier probe**
In diesem Code beispiel wird eine Panorama ansicht der 3D-Szene angezeigt und im Bildformat gespeichert.

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
