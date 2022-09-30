---
title: 在3D场景上创建一个鱼眼镜头效果并保存在图像中
type: docs
weight: 20
url: /zh/net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/
description: 使用Aspose.3D for .NET API，开发人员可以在3D场景上创建鱼眼镜头效果，并将该视图保存为支持的图像格式。
---
{{% alert color="primary" %}}

使用[Aspose.3D for .NET API](https://products.aspose.com/3d/net/),开发人员可以在3D场景上创建鱼眼镜头效果，并将该视图保存为支持的图像格式。

{{% /alert %}}
## **打造鱼眼镜头效果**
在本文中，我们创建一个相机和两个光对象来捕获场景，还创建一个渲染目标，创建一个视口，并以多维数据集贴图作为输入执行鱼眼投影后处理，最后保存鱼眼纹理。`Renderer`类的`Execute`方法允许执行后处理效果并将结果保存到render target。
### **编程示例**
此代码示例在3D场景上创建一个鱼眼镜头效果，并保存为图像格式。

**C#**

{{< highlight "java" >}}

 string path = @"D:\Projects\glTF-Sample-Models\1.0\VC\glTF-Binary\VC.glb";

//load the scene

Scene scene = new Scene(path);

//create a camera for capturing the cube map

Camera cam = new Camera(ProjectionType.Perspective)

{

    NearPlane = 0.1,

    FarPlane = 200,

    RotationMode = RotationMode.FixedDirection

};

scene.RootNode.CreateChildNode(cam).Transform.Translation = new Vector3(5, 6, 0);



//create two lights to illuminate the scene

scene.RootNode.CreateChildNode(new Light() {LightType = LightType.Point}).Transform.Translation = new Vector3(-10, 7, -10);

scene.RootNode.CreateChildNode(new Light()

{

    Color = new Vector3(Color.CadetBlue)

}).Transform.Translation = new Vector3(49, 0, 49);



//create a renderer

using (var renderer = Renderer.CreateRenderer())

{

    //Create a cube map render target with depth texture, depth is required when rendering a scene.

    IRenderTexture rt = renderer.RenderFactory.CreateCubeRenderTexture(new RenderParameters(false), 512, 512);

    //create a 2D texture render target with no depth texture used for image processing

    IRenderTexture final = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(false, 32, 0, 0), 1024, 1024);



    //a viewport is required on the render target

    rt.CreateViewport(cam, RelativeRectangle.FromScale(0, 0, 1, 1));

    renderer.Render(rt);



    //execute the fisheye projection post-processing with the previous rendered cube map as input

    //the fisheye can have field of view more than 180 degree, so a cube map with all direction is required.

    PostProcessing fisheye = renderer.GetPostProcessing("fisheye");

    // we can change the fov to 360 instead of the default value 180.

    fisheye.FindProperty("fov").Value = 360.0;

    //Specify the cube map rendered from the scene as this post processing's input

    fisheye.Input = rt.Targets[0];

    //Execute the post processing effect and save the result to render target final

    renderer.Execute(fisheye, final);

    //save the texture into disk

    ((ITexture2D)final.Targets[0]).Save("fisheye.png", ImageFormat.Png);

}

{{< /highlight >}}
