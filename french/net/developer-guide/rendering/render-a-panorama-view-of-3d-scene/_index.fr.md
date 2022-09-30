---
title: Rendre une vue panoramique de 3D scène
type: docs
weight: 60
url: /fr/net/render-a-panorama-view-of-3d-scene/
description: En utilisant Aspose.3D for .NET API, les développeurs peuvent rendre une vue panoramique de la scène 3D et enregistrer cette vue dans les formats d'image pris en charge.
---
{{% alert color="primary" %}}

Utilisation[Aspose.3D for .NET API](https://products.aspose.com/3d/net/), Les développeurs peuvent rendre une vue panoramique de la scène 3D et enregistrer cette vue dans les formats d'image pris en charge.

{{% /alert %}}
## **Créer une vue Panorama**
Dans cet article, nous créons une caméra et deux objets Light pour capturer la scène, créer également une cible de rendu, créer un viewport et exécuter le post-traitement de projection équirectangulaire avec la carte de cube en entrée et enfin enregistrer la texture Panorama. La méthode `Execute` de la classe `Renderer` permet d'exécuter l'effet de post-traitement et d'enregistrer le résultat pour rendre la cible.
### **Échantillon de programmation**
Cet exemple de code rend une vue Panorama de la scène 3D et enregistre dans le format d'image.

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
