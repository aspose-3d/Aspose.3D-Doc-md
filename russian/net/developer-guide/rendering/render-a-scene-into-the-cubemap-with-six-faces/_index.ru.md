---
title: Вправить сцену в кубемап с шестью лицами
type: docs
weight: 70
url: /ru/net/render-a-scene-into-the-cubemap-with-six-faces/
description: Используя Aspose.3D for .NET API, разработчики могут визуализировать сцену в cubemap с шестью лицами и сохранить все грани в поддерживаемых форматах изображений.
---
{{% alert color="primary" %}}

Используя[Aspose.3D for .NET 0761234881](https://products.aspose.com/3d/net/), Разработчики могут визуализировать сцену в cubemap с шестью лицами и сохранять все грани в поддерживаемые форматы изображений.

{{% /alert %}}
## **Захватите кубемап с шестью лицами**
В этой статье мы создаем камеру и два световых объекта, чтобы запечатлеть cubemap, также создаем цель визуализации cubemap с текстурой глубины, создаем видовой экран и, наконец, получаем текстуру cubemap. Класс `ITextureCubema`p извлекает текстуру cubemap, а класс `CubeFaceData` позволяет получить доступ к граням cubemap, а затем экспортировать в поддерживаемый формат изображения.
### **Образец программирования**
В этом примере кода сцена превращается в cubemap с шестью гранями и экспортируется в формат изображения.

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
