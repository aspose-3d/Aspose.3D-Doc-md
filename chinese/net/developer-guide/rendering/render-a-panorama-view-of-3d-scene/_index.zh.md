---
title: 渲染3D场景的全景视图
type: docs
weight: 60
url: /zh/net/render-a-panorama-view-of-3d-scene/
description: 使用Aspose.3D for .NET API，开发人员可以渲染3D场景的全景视图，并将该视图保存为支持的图像格式。
---
{{% alert color="primary" %}}

使用[Aspose.3D for .NET API](https://products.aspose.com/3d/net/),开发人员可以渲染3D场景的全景视图，并将该视图保存为支持的图像格式。

{{% /alert %}}
## **创建全景视图**
在本文中，我们创建一个相机和两个光对象来捕获场景，还创建一个渲染目标，创建一个视口，并使用立方体贴图作为输入执行等矩形投影后处理，最后保存全景纹理。`Renderer`类的`Execute`方法允许执行后处理效果并将结果保存到render target。
### **编程示例**
此代码示例呈现3D场景的全景视图并保存为图像格式。

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

    IRenderTexture final = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(false, 32, 0, 0), 1024 * 3 , 1024);



    //a viewport is required on the render target

    rt.CreateViewport(cam, RelativeRectangle.FromScale(0, 0, 1, 1));

    renderer.Render(rt);



    //execute the equirectangular projection post-processing with the previous rendered cube map as input

    PostProcessing equirectangular = renderer.GetPostProcessing("equirectangular");

    //Specify the cube map rendered from the scene as this post processing's input

    equirectangular.Input = rt.Targets[0];

    //Execute the post processing effect and save the result to render target final

    renderer.Execute(equirectangular, final);

    //save the texture into disk

    ((ITexture2D)final.Targets[0]).Save("panorama.png", ImageFormat.Png);

}

{{< /highlight >}}
