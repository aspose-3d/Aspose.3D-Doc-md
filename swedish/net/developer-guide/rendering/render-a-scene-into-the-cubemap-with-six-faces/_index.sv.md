---
title: Rensar en scen i kubekartan med sex ansikten
type: docs
weight: 70
url: /sv/net/render-a-scene-into-the-cubemap-with-six-faces/
description: Använder Aspose. 3D for .NET API, utvecklare kan göra en scen in i kubemappen med sex ansikten och spara alla ansikten i de bildformat som stöds.
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for .NET API](https://products.aspose.com/3d/net/) kan utvecklare göra en scen in i kubemappen med sex sidor och spara alla ansikten i de bildformat som stöds.

{{% /alert %}}
##  **Fånga en kubekarta med sex ansikten**
I den här artikeln skapar vi en kamera och två Ljus objekt för att fånga kubemappen, Skapa också en kubemap render mål med djup konsistens, skapa en visning och slutligen få kubemap textur. `ITextureCubema`-klassen hämtar kubemap-texturen och `CubeFaceData`-klassen tillåter åtkomst till kubemappens sidor, och sedan exportera till det bildformat som stöds.
###  **Programmeringsprova**
Det här kodexemplet gör en scen in i kubekartan med sex ansikten och exporterar till bildformatet.

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
