---
title: Rendera en Panorama vy av 3D scena
type: docs
weight: 60
url: /sv/net/render-a-panorama-view-of-3d-scene/
description: Med Aspose.3D for .NET API, utvecklare kan ge en panoramavy av 3D scen och spara den vyn i de bildformat som stöds.
---
{{% alert color="primary" %}}

Användning[Aspose.3D for .NET API](https://products.aspose.com/3d/net/), Kan utvecklare återge en panoramavy av 3D scen och spara den vyn i de bildformat som stöds.

{{% /alert %}}
## **Skapa en panoramavy**
I den här artikeln skapar vi en kamera och två Ljus objekt för att fånga scenen, också skapa en rendering mål, skapa en visningsport och kör den ekvattangulära projektionen efterbehandling med kubenkartan som inmatning och slutligen spara Panen Orama konsistens. `Execute`-metoden `Renderer`-klass gör det möjligt att utföra efterbehandlingseffekten och spara resultatet för att göra mål.
### **Programmeringsprova**
Detta kodexempel ger en Panorama vy av 3D scen och spara i bildformatet.

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
