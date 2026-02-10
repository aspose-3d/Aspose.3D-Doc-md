---
title: Aplicar efectos visuales al guardar las vistas 3D
type: docs
weight: 10
url: /es/python-net/apply-visual-effects-on-saving-3d-views/
description: Usando Aspose.3D for Python via .NET API, los desarrolladores pueden aplicar efectos visuales en 3D Vistas antes de guardar en la imagen. Estos efectos visuales también se conocen como efectos de posprocesamiento o filtros que se aplican en tiempo real a todo lo que se muestra en la vista 3D.
---
{{% alert color="primary" %}}

Con [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), los desarrolladores pueden aplicar efectos visuales en las vistas de 3D antes de guardar la imagen. Estos efectos visuales también se conocen como efectos de posprocesamiento o filtros que se aplican en tiempo real a todo lo que se muestra en la vista 3D.

{{% /alert %}}
##  **Aplicar efectos visuales en la vista 3D**
El método [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) de la clase [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) permite crear cualquier efecto visual admitido. La clase `Renderer` ofrece un miembro [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) para aplicar varios filtros, el método Add de la clase `PostProcessings` permite incorporar un filtro antes de renderizar.
###  **Muestra de programación**
Este ejemplo de código aplica el efecto visual en una vista 3D.

{{< highlight "python" >}}
from aspose import pycore
from aspose.pydrawing import Color
from aspose.pydrawing.imaging import ImageFormat
from aspose.threed import Scene
from aspose.threed.entities import Camera, Light, LightType
from aspose.threed.render import ITexture2D, RenderParameters, Renderer
from aspose.threed.utilities import RelativeRectangle, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load an existing 3D scene
scene = Scene("data-dir"  + "scene.obj")
#  Create an instance of the camera
camera = Camera()
scene.root_node.create_child_node("camera", camera).transform.translation = Vector3(2, 44, 66)
#  Set the target
camera.look_at = Vector3(50, 12, 0)
light = Light()
light.color = Vector3(Color.white)
light.light_type = LightType.POINT
#  Create a light
scene.root_node.create_child_node("light", light).transform.translation = Vector3(26, 57, 43)
#  The CreateRenderer will create a hardware OpenGL-backend renderer, more renderer will be added in the future
#  And some internal initializations will be done.
#  When the renderer left using the scope, the unmanaged hardware resources will also be disposed
with Renderer.create_renderer() as renderer:
    renderer.enable_shadows = False
    #  Create a new render target that renders the scene to texture(s)
    #  Use default render parameters
    #  And one output targets
    #  Size is 1024 x 1024
    #  This render target can have multiple render output textures, but here we only need one output.
    #  The other textures and depth textures are mainly used by deferred shading in the future.
    #  But you can also access the depth texture through IRenderTexture.DepthTeture
    with renderer.render_factory.create_render_texture(RenderParameters(), 1, 1024, 1024) as rt:
        rectangle = RelativeRectangle()
        rectangle.scale_width = 1.0
        rectangle.scale_height = 1 .0
        #  This render target has one viewport to render, the viewport occupies the 100% width and 100% height
        vp = rt.create_viewport(camera, rectangle)
        #  Render the target and save the target texture to external file
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "Original_viewport_out.png", ImageFormat.png)
        #  Create a post-processing effect
        pixelation = renderer.get_post_processing("pixelation")
        renderer.post_processings.append(pixelation)
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "VisualEffect_pixelation_out.png", ImageFormat.png)
        #  Clear previous post-processing effects and try another one
        grayscale = renderer.get_post_processing("grayscale")
        renderer.post_processings.clear()
        renderer.post_processings.append(grayscale)
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "VisualEffect_grayscale_out.png", ImageFormat.png)
        #  We can also combine post-processing effects
        renderer.post_processings.clear()
        renderer.post_processings.append(grayscale)
        renderer.post_processings.append(pixelation)
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "VisualEffect_grayscale+pixelation_out.png", ImageFormat.png)
        #  Clear previous post-processing effects and try another one
        edgedetection = renderer.get_post_processing("edge-detection")
        renderer.post_processings.clear()
        renderer.post_processings.append(edgedetection)
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "VisualEffect_edgedetection_out.png", ImageFormat.png)
        #  Clear previous post-processing effects and try another one
        blur = renderer.get_post_processing("blur")
        renderer.post_processings.clear()
        renderer.post_processings.append(blur)
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "VisualEffect_blur_out.png", ImageFormat.png)

{{< /highlight >}}
