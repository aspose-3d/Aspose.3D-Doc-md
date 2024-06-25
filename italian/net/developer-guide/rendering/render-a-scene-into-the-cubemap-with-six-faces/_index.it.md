---
title: Renderi una scena nella cubemap con sei facce
type: docs
weight: 70
url: /it/net/render-a-scene-into-the-cubemap-with-six-faces/
description: Utilizzando Aspose.3D for .NET API, gli sviluppatori possono visualizzare una scena nella cubemap con sei facce e salvare tutti i volti nei formati di immagine supportati.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), gli sviluppatori possono eseguire il rendering di una scena nella cubemap con sei facce e salvare tutti i volti nei formati di immagine supportati.

{{% /alert %}}
##  **Cattura una cubemap con sei facce**
In questo articolo, creiamo una fotocamera e due oggetti Light per catturare la cubemap, creare anche un obiettivo di rendering cubemap con texture di profondità, creare un viewport e infine ottenere la texture cubemap. La classe `ITextureCubema`p recupera la texture della cubemap e la classe `CubeFaceData` consente di accedere alle facce della cubemap, quindi di esportare nel formato dell'immagine supportato.
###  **Campione di programmazione**
Questo esempio di codice esegue il rendering di una scena nella cubemap con sei facce ed esporta nel formato dell'immagine.

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
