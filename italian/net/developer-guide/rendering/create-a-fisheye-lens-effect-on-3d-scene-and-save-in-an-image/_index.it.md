---
title: Creare un effetto lente Fish-eye sulla scena 3D e salvare in un'immagine
type: docs
weight: 20
url: /it/net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/
description: Utilizzando Aspose.3D for .NET API, gli sviluppatori possono creare un effetto obiettivo Fisheye sulla scena 3D e salvare quella visualizzazione nei formati di immagine supportati.
---
{{% alert color="primary" %}}

Utilizzo[Aspose.3D for .NET API](https://products.aspose.com/3d/net/), Gli sviluppatori possono creare un effetto obiettivo Fisheye sulla scena 3D e salvare tale visualizzazione nei formati di immagine supportati.

{{% /alert %}}
## **Crea un effetto obiettivo Fisheye**
In questo articolo, creiamo una fotocamera e due oggetti Light per catturare la scena, creare anche un target di rendering, creare un viewport ed eseguire la post-elaborazione della proiezione di Fisheye con la mappa del cubo come input e infine salvare la texture Fisheye. Il metodo `Execute` della classe `Renderer` consente di eseguire l'effetto post-elaborazione e salvare il risultato per rendere il target.
### **Campione di programmazione**
Questo esempio di codice crea un effetto obiettivo Fisheye sulla scena 3D e salva nel formato dell'immagine.

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
