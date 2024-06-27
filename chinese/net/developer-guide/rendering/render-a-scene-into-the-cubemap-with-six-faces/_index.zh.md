---
title: 用六个面将场景渲染到立方体图中
type: docs
weight: 70
url: /zh/net/render-a-scene-into-the-cubemap-with-six-faces/
description: 使用 Aspose.3D for .NET API，开发人员可以将具有六个面的场景渲染到cubemap中，并将所有面保存为支持的图像格式。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET API](https://products.aspose.com/3d/net/)，开发人员可以将场景渲染到具有六个面的cubemap中，并将所有面保存为支持的图像格式。

{{% /alert %}}
##  **捕获具有六个面孔的立方体地图**
在本文中，我们创建了一个相机和两个光对象来捕获立方体贴图，还创建了一个带有深度纹理的立方体贴图渲染目标，创建了一个视口，最后获得了立方体贴图纹理。`ITextureCubema`p类检索立方体贴图纹理，`CubeFaceData` 类允许访问立方体贴图的面，然后导出为支持的图像格式。
###  **编程示例**
此代码示例将场景渲染到具有六个面的cubemap中，并导出为图像格式。

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

    //a viewport is required on the render target

    rt.CreateViewport(cam, RelativeRectangle.FromScale(0, 0, 1, 1));

    renderer.Render(rt);

    //now lets get the cubemap texture

    ITextureCubemap cubemap = rt.Targets[0] as ITextureCubemap;

    //we can directly save each face to disk by specifing the file name

    CubeFaceData<string> fileNames = new CubeFaceData<string>()

    {

        Right = "right.png",

        Left = "left.png",

        Back = "back.png",

        Front = "front.png",

        Bottom = "bottom.png",

        Top = "top.png"

    };

    //and call Save method

    cubemap.Save(fileNames, ImageFormat.Png);

    //or we just need to use the render result in memory, we can save it to CubeFaceData<Bitmap>

    //CubeFaceData<Bitmap> bitmaps = new CubeFaceData<Bitmap>();

    //cubemap.Save(bitmaps);

    //bitmaps.Back.Save("back.bmp", ImageFormat.Bmp);

}

{{< /highlight >}}
