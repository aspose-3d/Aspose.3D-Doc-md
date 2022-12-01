---
title: Rendern Sie eine Panorama ansicht der Szene 3D
type: docs
weight: 60
url: /de/net/render-a-panorama-view-of-3d-scene/
description: Mithilfe der Aspose.3D for .NET APIkönnen Entwickler eine Panorama ansicht der 3D-Szene rendern und diese Ansicht in den unterstützten Bildformaten speichern.
---
{{% alert color="primary" %}}

Verwendung[Aspose.3D for .NET API](https://products.aspose.com/3d/net/)Entwickler können eine Panorama ansicht der 3D-Szene rendern und diese Ansicht in den unterstützten Bildformaten speichern.

{{% /alert %}}
## **Erstellen Sie eine Panorama-Ansicht**
In diesem Artikel erstellen wir eine Kamera und zwei Licht objekte, um die Szene zu erfassen, erstellen auch ein Render ziel, erstellen ein Ansicht fenster und führen die äqui rechteckige Projektions post verarbeitung mit der Würfel karte als Eingabe aus und speichern schließlich die Panorama-Textur. Die `Execute`-Methode der `Renderer`-Klasse ermöglicht es, den Nach bearbeitungs effekt auszuführen und das Ergebnis zu speichern, um das Ziel zu rendern.
### **Programmier probe**
Dieses Code beispiel bietet eine Panorama ansicht der Szene 3D und speichert im Bildformat.

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
