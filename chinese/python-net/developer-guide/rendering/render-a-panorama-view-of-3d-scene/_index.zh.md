---
title: 渲染 3D 场景的全景视图
type: docs
weight: 60
url: /zh/python-net/render-a-panorama-view-of-3d-scene/
description: 使用 Aspose.3D for Python via .NET API，开发人员可以渲染 3D 场景的全景视图，并将该视图保存为支持的图像格式。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for Python via .NET API](https:#products.aspose.com/3d/python-net/)，开发人员可以渲染 3D 场景的全景视图，并将该视图保存为支持的图像格式。

{{% /alert %}}
##  **创建全景视图**
在本文中，我们创建了一个相机和两个灯光对象来捕捉场景，还创建了一个渲染目标，创建了一个视口，并以立方体贴图作为输入执行了等矩形投影后处理，最后保存了全景纹理。`Renderer` 类的 `execute` 方法允许执行后处理效果并将结果保存到呈现目标。
###  **编程示例**
此代码示例呈现 3D 场景的全景视图并保存为图像格式。

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
