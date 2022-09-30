---
title: 在3D场景上创建一个鱼眼镜头效果并保存在图像中
type: docs
weight: 20
url: /zh/python-net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/
description: 使用Aspose.3D进行Python via .NET API，开发人员可以在3D场景上创建鱼眼镜头效果，并将该视图保存为支持的图像格式。
---
{{% alert color="primary" %}}

使用[Aspose.3D Python via .NET API](https:#products.aspose.com/3d/python-net/),开发人员可以在3D场景上创建鱼眼镜头效果，并将该视图保存为支持的图像格式。

{{% /alert %}}
## **打造鱼眼镜头效果**
在本文中，我们创建一个相机和两个光对象来捕获场景，还创建一个渲染目标，创建一个视口，并以多维数据集贴图作为输入执行鱼眼投影后处理，最后保存鱼眼纹理。`Renderer`类的`execute`方法允许执行后处理效果并将结果保存到render target。
### **编程示例**
此代码示例在3D场景上创建一个鱼眼镜头效果，并保存为图像格式。

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
