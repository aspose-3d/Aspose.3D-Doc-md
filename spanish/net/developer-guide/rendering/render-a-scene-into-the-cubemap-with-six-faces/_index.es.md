---
title: Rinde una escena en el cubemap con seis caras
type: docs
weight: 70
url: /es/net/render-a-scene-into-the-cubemap-with-six-faces/
description: Usando Aspose.3D for .NET API, los desarrolladores pueden representar una escena en el cubemap con seis caras y guardar todas las caras en los formatos de imagen compatibles.
---
{{% alert color="primary" %}}

Uso[Aspose.3D for .NET API](https://products.aspose.com/3d/net/), Los desarrolladores pueden renderizar una escena en el cubemap con seis caras y guardar todas las caras en los formatos de imagen compatibles.

{{% /alert %}}
## **Captura un cubemap con seis caras**
En este artículo, creamos una cámara y dos objetos de luz para capturar el cubemap, también creamos un objetivo de representación de cubemap con textura de profundidad, creamos una ventana gráfica y finalmente obtenemos la textura del cubemap. La clase `ITextureCubema`p recupera la textura cubemap y la clase `CubeFaceData` permite acceder a las caras del cubemap y luego exportar al formato de imagen admitido.
### **Muestra de programación**
Este ejemplo de código representa una escena en el cubemap con seis caras y la exportación al formato de imagen.

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
