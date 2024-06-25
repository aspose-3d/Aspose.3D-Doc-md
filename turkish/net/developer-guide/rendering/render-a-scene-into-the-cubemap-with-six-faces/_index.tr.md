---
title: Raltı yüzü ile cubemap içine bir sahne ender
type: docs
weight: 70
url: /tr/net/render-a-scene-into-the-cubemap-with-six-faces/
description: Aspose.3D for .NET API kullanarak, geliştiriciler altı yüz ile cubemap içine bir sahne oluşturabilir ve tüm yüzleri desteklenen görüntü formatlarına kaydedebilir.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET API](https://products.aspose.com/3d/net/) kullanarak, geliştiriciler altı yüz ile cubemap içine bir sahne oluşturabilir ve tüm yüzleri desteklenen görüntü formatlarına kaydedebilir.

{{% /alert %}}
##  **Capture altı yüzlü bir cubemap**
Bu makalede, cubemap'ı yakalamak için bir kamera ve iki ışık nesnesi oluşturuyoruz, ayrıca derinlik dokusu ile bir cubemap oluşturma hedefi oluşturuyoruz, bir bakış açısı oluşturuyoruz ve sonunda cubemap dokusunu alıyoruz. `ITextureCubema`p sınıfı, cubemap dokusunu ve `CubeFaceData` sınıfını alır ve daha sonra desteklenen görüntü formatına dışa aktarır.
###  **Programming ample ample**
Tkod örneği, altı yüz ile cubemap içine bir sahne oluşturur ve görüntü formatına aktarır.

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
