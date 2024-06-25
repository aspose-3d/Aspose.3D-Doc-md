---
title: Skapa en objektiveffekt på 3D och spara i en bild
type: docs
weight: 20
url: /sv/net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/
description: Använder Aspose. 3D for .NET API, Utvecklare kan skapa en Fisheye-linseffekt på 3D-scenen och spara den vyn i de bildformat som stöds.
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for .NET API](https://products.aspose.com/3d/net/) kan utvecklare skapa en Fisheye-linseffekt på 3D-scenen och spara den vyn i de bildformat som stöds.

{{% /alert %}}
##  **Skapa en Fisheye-linseffekt**
I den här artikeln skapar vi en kamera och två Ljus objekt för att fånga scenen, också skapa en rendering mål, skapa en visningsplats och utför Fisheye projektion efter bearbetning med kubenkartan som inmatning och slutligen spara texten Fisheye. - Ja, jag vet inte. `Execute`-metoden för `Renderer`-klassen gör det möjligt att köra efterbehandlingseffekten och spara resultatet för att visa målet.
###  **Programmeringsprova**
Det här kodexemplet skapar en Fisheye linseffekt på 3D-scenen och sparar i bildformatet.

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
