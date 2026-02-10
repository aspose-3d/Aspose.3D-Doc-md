---
title: Capture the Viewports of 3D Scene and Render to a Texture or Window
type: docs
weight: 20
url: /python-net/capture-the-viewports-of-3d-scene-and-render-to-a-texture-or-window/
description: Each 3D scene can comprise of any number of viewports. Using Aspose.3D for Python via .NET API, developers can capture one or more viewports in a single screenshot. They may render it in the GUI based .NET application or an image.
---

{{% alert color="primary" %}}

Each 3D scene can comprise of any number of viewports. Using [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), developers can capture one or more viewports in a single screenshot. They may render it in the GUI based .NET application or an image.

{{% /alert %}}
## **Capturing and Rendering the Viewports of 3D Scene**
The `create_render_texture` and `create_render_window` methods exposed by the [`RenderFactory`](https://reference.aspose.com/3d/net/aspose.threed.render/renderfactory) class can be used to create a new render target that renders the scene to a texture or Window.
### **Programming Sample**
This code example captures a viewport of 3D Scene and renders it in two different ways.

{{< highlight "python" >}}
from aspose import pycore
from aspose.pydrawing import Color, ImageFormat
from aspose.threed import Scene
from aspose.threed.entities import Camera, Light, LightType, ProjectionType, RotationMode
from aspose.threed.render import ITexture2D, RenderParameters, Renderer
from aspose.threed.utilities import RelativeRectangle, Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
#  load a scene
scene = Scene("data-dir"  + "VirtualCity.glb")
camera = Camera(ProjectionType.PERSPECTIVE)
camera.near_plane = 0.1
camera.far_plane = 200.0
camera.rotation_mode = RotationMode.FIXED_DIRECTION
#  create a camera for capturing a cube map
cam = camera
cam.transform.translation = Vector3(5, 6, 0)
#  create two lights to illuminate the scene
light = Light()
light.light_type = LightType.POINT
scene.root_node.create_child_node(light).transform.translation = Vector3(-10, 7, -10)
light2 = Light()
light2.color = Vector3(Color.cadet_blue)
scene.root_node.create_child_node(light2).transform.translation = Vector3(49, 0, 49)
#  create a renderer
with Renderer.create_renderer() as renderer:
    #  Create a cube map render target with depth texture, depth is required when rendering a scene.
    rt = renderer.render_factory.create_cube_render_texture(RenderParameters(False), 512, 512)
    #  create a 2D texture render target with no depth texture used for image processing
    final = renderer.render_factory.create_render_texture(RenderParameters(False), 32, 0), 1024 * 3, 1024)
    #  a viewport is required on a render target
    rt.create_viewport(cam, RelativeRectangle.from_scale(0, 0, 1, 1))
    renderer.render(rt)
    #  execute fisheye projection post-processing with the previous rendered cube map as input
    fisheye = renderer.get_post_processing("fisheye")
    #  fisheye can have field of view more than 180 degree, so a cube map with all direction is required.
    fisheye.find_property("fov").value = 360.0
    #  Specify the cube map rendered from the scene as this post processing's input
    fisheye.input = rt.targets[0]
    #  Execute the post processing effect and save the result to render target final
    renderer.execute(fisheye, final)
    #  save the texture into disk
    pycore.cast(ITexture2D, final.targets[0]).save("out"  + "fisheye.png", ImageFormat.png)
{{< /highlight >}}
