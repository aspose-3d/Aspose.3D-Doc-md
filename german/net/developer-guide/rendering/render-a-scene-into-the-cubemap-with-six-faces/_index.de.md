---
title: Rendern Sie eine Szene in die Cubemap mit sechs Gesichtern
type: docs
weight: 70
url: /de/net/render-a-scene-into-the-cubemap-with-six-faces/
description: Mithilfe der Aspose.3D for .NET APIkönnen Entwickler eine Szene mit sechs Gesichtern in die Cubemap rendern und alle Gesichter in den unterstützten Bildformaten speichern.
---
{{% alert color="primary" %}}

Verwendung[Aspose.3D for .NET API](https://products.aspose.com/3d/net/)Entwickler können eine Szene mit sechs Gesichtern in die Cubemap rendern und alle Gesichter in den unterstützten Bildformaten speichern.

{{% /alert %}}
## **Erfassen Sie eine Cubemap mit sechs Gesichtern**
In diesem Artikel erstellen wir eine Kamera und zwei Licht objekte, um die Cubemap zu erfassen, erstellen auch ein Cubemap-Render ziel mit Tiefen textur, erstellen ein Ansicht fenster und erhalten schließlich die Cubemap-Textur. Die `ITextureCubema`p-Klasse ruft die Cubemap-Textur ab und die `CubeFaceData`-Klasse ermöglicht den Zugriff auf Flächen der Cubemap und den Export in das unterstützte Bildformat.
### **Programmier probe**
In diesem Code beispiel wird eine Szene mit sechs Flächen in die Cubemap gerendert und in das Bildformat exportiert.

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
