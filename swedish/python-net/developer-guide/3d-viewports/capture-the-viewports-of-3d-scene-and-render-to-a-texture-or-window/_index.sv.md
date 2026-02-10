---
title: Fånga vyer för 3D Scene och teckning till en textur eller fönster
type: docs
weight: 20
url: /sv/python-net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: Varje 3Dscen kan omfatta ett antal visningar. Med Aspose.3D for Python via .NET API kan utvecklare fånga en eller flera vyer i en enda skärmbild. De kan göra det i GUI-baserade .NET-program eller en bild.
---
{{% alert color="primary" %}}

Varje 3Dscen kan omfatta ett antal visningar. Med [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/) kan utvecklare fånga en eller flera vyer i en enda skärmbild. De kan göra det i GUI-baserade .NET-program eller en bild.

{{% /alert %}}
##  **Fånga och redigera vyer för 3D Scene**
Metoderna `create_render_texture` och `create_render_window` som exponeras av klassen [`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory) kan användas för att skapa ett nytt mål för rendering som visar scenen till - en textur eller fönster.
###  **Programmeringsprova**
Det här kodexemplet tar en visningsport av 3D och visar den på två olika sätt.

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
#  The CreateRenderer will create a hardware OpenGL-backend renderer
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
    #  Use CreateRenderWindow method to render in window, like:
    #  Window = renderer.RenderFactory.CreateRenderWindow(new RenderParameters(), Handle);
    with renderer.render_factory.create_render_texture(RenderParameters(), 1, 1024, 1024) as rt:
        rectangle = RelativeRectangle()
        rectangle.scale_width = 1.0
        rectangle.scale_height = 1 .0
        #  This render target has one viewport to render, the viewport occupies the 100% width and 100% height
        vp = rt.create_viewport(camera, rectangle)
        #  Render the target and save the target texture to external file
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "file-1viewports_out.png", ImageFormat.png)
        rectangle2 = RelativeRectangle()
        rectangle2.scale_width = 0.5
        rectangle2.scale_height = 1 .0
        #  Now let's change the previous viewport only uses the half left side(50% width and 100% height)
        vp.area = rectangle2
        rectangle3 = RelativeRectangle()
        rectangle3.scale_x = 0.5
        rectangle3.scale_width = 0.5
        rectangle3.scale_height = 1 .0
        #  And create a new viewport that occupies the 50% width and 100% height and starts from 50%
        #  Both of them are using the same camera, so the rendered content should be the same
        rt.create_viewport(camera, rectangle3)
        #  But this time let's increase the field of view of the camera to 90 degree so it can see more part of the scene
        camera.field_of_view = 90.0
        renderer.render(rt)
        pycore.cast(ITexture2D, rt.targets[0]).save("out"  + "file-2viewports_out.png", ImageFormat.png)

{{< /highlight >}}
