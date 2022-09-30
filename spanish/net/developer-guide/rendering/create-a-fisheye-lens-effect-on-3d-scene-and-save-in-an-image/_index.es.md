---
title: Crear un efecto de lente ojo de pez en la escena 3D y guardar en una imagen
type: docs
weight: 20
url: /es/net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/
description: Usando Aspose.3D for .NET API, los desarrolladores pueden crear un efecto de lente de ojo de pez en la escena 3D y guardar esa vista en los formatos de imagen compatibles.
---
{{% alert color="primary" %}}

Uso[Aspose.3D for .NET API](https://products.aspose.com/3d/net/), Los desarrolladores pueden crear un efecto de lente Fisheye en la escena 3D y guardar esa vista en los formatos de imagen compatibles.

{{% /alert %}}
## **Crea un efecto de lente de ojo de pez**
En este artículo, creamos una cámara y dos objetos de luz para capturar la escena, también creamos un objetivo de renderizado, creamos una ventana gráfica y ejecutamos el postprocesamiento de proyección de ojo de pez con el mapa de cubo como entrada y finalmente guardamos la textura de ojo de pez. El método `Execute` de la clase `Renderer` permite ejecutar el efecto de procesamiento posterior y guardar el resultado para representar el objetivo.
### **Muestra de programación**
Este ejemplo de código crea un efecto de lente Fisheye en la escena 3D y guárdelo en el formato de imagen.

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
