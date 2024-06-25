---
title: Рендеринг панорамного вида сцены 3D
type: docs
weight: 60
url: /ru/net/render-a-panorama-view-of-3d-scene/
description: Используя Aspose.3D for .NET API, разработчики могут отрисовывать панораму сцены 3D и сохранять этот вид в поддерживаемых форматах изображений.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), разработчики могут отобразить панораму сцены 3D и сохранить этот вид в поддерживаемых форматах изображений.

{{% /alert %}}
##  **Создать вид Panorama**
В этой статье мы создадим камеру и два объекта Light для захвата сцены, также создадим мишень рендеринга, создадим видовой экран и выполним эквипрямоугольную постобработку проекции с картой куба в качестве входных данных и, наконец, сохраним текстуру Panorama. Метод `Execute` класса `Renderer` позволяет выполнить эффект пост-обработки и сохранить результат для рендеринга цели.
###  **Образец программирования**
Этот пример кода отображает панораму сцены 3D и сохраняет ее в формате изображения.

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
