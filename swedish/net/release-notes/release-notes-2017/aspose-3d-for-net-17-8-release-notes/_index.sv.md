---
title: Aspose.3D for .NET 17,8 Utgivning
type: docs
weight: 50
url: /sv/net/aspose-3d-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17,8](https://www.nuget.org/packages/Aspose.3D/17.8.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-279|Rendera scen till en kub karta med 6 ansikten.|Ny funktion|
|THREEDNET-280|Lägg till efterbehandling av ekvivalent projektion.|Ny funktion|
|THREEDNET-281|Render kub karta till fisheye.|Ny funktion|
|THREEDNET-276|Felaktig omvandling av OBJ till GLTF och GLB.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Metoder markerade som föråldrade och kommer att tas bort i slutet av detta år 2017.**
Före den 17.8 alla textur enheter (används av renderaren) representeras av gränssnittet ITextureUnit men denna design fungerar inte bra för kub kartan och 3D textur i framtiden (inte genomfört ännu), så dessa metoder är alla markerade som föråldrade, För att säkerställa att koden inte bryter kompilatorn, Utvecklarna bör använda metoderna med samma namn från ITexture1D/ITexture2D/ITextureCubemap.

**C#**

{{< highlight "java" >}}

 interface ITextureUnit

{

    void Load(TextureData bitmap);

    void Save(string path, ImageFormat format);

    void Save(Bitmap bitmap);

    Bitmap ToBitmap();

} 

{{< /highlight >}}
#### **Tillagd ny enum typ Aspose.ThreeD.Render.CubeFace.**
Denna typ fungerar med Aspose.ThreeD.Render.CubeFaceData.<>Och Aspose.ThreeD.Render.ITextureCubemap för att få åtkomst till data enligt kubemappens yta.

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Each face of the cube map texture 

/// </summary>

public enum CubeFace

{

    /// <summary>

    /// The +X face

    /// </summary>

    PositiveX,

    /// <summary>

    /// The -X face

    /// </summary>

    NegativeX,

    /// <summary>

    /// The +Y face

    /// </summary>

    PositiveY,

    /// <summary>

    /// The -Y face

    /// </summary>

    NegativeY,

    /// <summary>

    /// The +Z face

    /// </summary>

    PositiveZ,

    /// <summary>

    /// The -Z face

    /// </summary>

    NegativeZ

}

{{< /highlight >}}
#### **Lagt till ny klass Aspose.ThreeD.Render.CubeFaceData<>**
Denna klass är en generisk klass för att beskriva data per kubemap ansikte som filnamn eller bitmap.
#### **Tillagd ny klass Aspose.ThreeD.Render.ITextureCubemap**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Cube map texture

/// </summary>

public interface ITextureCubemap : ITextureUnit

{

    /// <summary>

    /// Load texture content from specified files

    /// </summary>

    /// <param name="fileNames"></param>

    void Load(CubeFaceData<string> fileNames);

    /// <summary>

    /// Load texture content from specified <see cref="TextureData"/>

    /// </summary>

    /// <param name="data"></param>

    void Load(CubeFaceData<TextureData> data);

    /// <summary>

    /// Load the data into specified face

    /// </summary>

    /// <param name="face"></param>

    /// <param name="data"></param>

    void Load(CubeFace face, TextureData data);

    /// <summary>

    /// Save the cube's sides texture content to external files.

    /// </summary>

    /// <param name="path">File names to save.</param>

    /// <param name="format">Image format</param>

    void Save(CubeFaceData<string> path, ImageFormat format);

    /// <summary>

    /// Save the texture content to memory.

    /// </summary>

    /// <param name="bitmap">Result bitmap to save.</param>

    void Save(CubeFaceData<Bitmap> bitmap);

    /// <summary>

    /// Save the specified side to memory

    /// </summary>

    /// <param name="side"></param>

    /// <param name="bitmap"></param>

    void Save(CubeFace side, Bitmap bitmap);

    /// <summary>

    /// Convert the texture unit to <see cref="Bitmap"/> instance

    /// </summary>

    Bitmap ToBitmap(CubeFace side);    

}

{{< /highlight >}}

**C#**

{{< highlight "java" >}}

 //The model used in this sample can be found at https://github.com/KhronosGroup/glTF-Sample-Models/tree/master/1.0/VC/glTF-Binary

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

    CubeFaceData<Bitmap> bitmaps = new CubeFaceData<Bitmap>();

    cubemap.Save(bitmaps);

    bitmaps.Back.Save("back.bmp", ImageFormat.Bmp);

}

{{< /highlight >}}
#### **Tillagd ny klass Aspose.ThreeD.Render.ITexture1D**
Det här gränssnittet används för att representera ett 1D- texturobjekt
#### **Tillagd ny klass Aspose.ThreeD.Render.ITexture2D**
Det här gränssnittet används för att representera ett 2D- texturobjekt
#### **Lagt till nya metoder till klass Aspose.ThreeD.Render.RenderFakty:**
**C#**

{{< highlight "java" >}}

 // this is an overloaded version for method IRenderTexture CreateRenderTexture(Aspose.ThreeD.Render.RenderParameters parameters, int targets, int width, int height) with targets to 1

public Aspose.ThreeD.Render.IRenderTexture CreteRenderTexture(Aspose.ThreeD.Render.RenderParameters parameters, int width, int height)

//Create a render target that will render the scene into a cube map

public Aspose.ThreeD.Render.IRenderTexture CreateCubeRenderTexture(Aspose.ThreeD.Render.RenderParameters parameters, int width, int height)

// allow user to create ITexture1D/ITexture2D/ITextureCubemap manually

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit(Aspose.ThreeD.Render.TextureType textureType)

{{< /highlight >}}
#### **Lagt till ny metod i klass Aspose.ThreeD.Render.Render:**
I de tidigare versionerna kan postbehandlingen endast användas genom att tillhandahålla en kedja av efterbehandlingseffekter till Aspose.ThreeD. Render. Renderer. PostProcessings, nu med denna metod användaren kan manuellt utföra efterbehandlingsförfarandet, detta är användbart i de nya funktionerna THREEDNET-280 och THREEDNET-281, innebär att du kan göra en kubekarta till en panoramabild eller fisheye-bild.

**C#**

{{< highlight "java" >}}

 public void Execute(Aspose.ThreeD.Render.PostProcessing postProcessing, Aspose.ThreeD.Render.IRenderTarget result)

{{< /highlight >}}






#### **Skapa en panoramabild i 3D Scene**
Utvecklare kan använda tredje parts verktyg som tre.js/Pano2VR för att visualisera resultatet.

**C#**

{{< highlight "java" >}}

 //The model used in this sample can be found at https://github.com/KhronosGroup/glTF-Sample-Models/tree/master/1.0/VC/glTF-Binary

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







**Generera Fisheye linseffekt i 3D Scene**

**C#**

{{< highlight "java" >}}

 //The model used in this sample can be found at https://github.com/KhronosGroup/glTF-Sample-Models/tree/master/1.0/VC/glTF-Binary

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

**Lagt metoder för att strukturera Aspose.ThreeD.Utilities.FVector3:**

Detta är de två primitiva operationerna av vektorer.

**C#**

{{< highlight "java" >}}

 //Calculate the normalized vector of the FVector3, equivalent implementation of Vector3.Normalize

public Aspose.ThreeD.Utilities.FVector3 Normalize()

//Calculate the cross product of two FVector3, equivalent implementation of Vector3.Cross

public Aspose.ThreeD.Utilities.FVector3 Cross(Aspose.ThreeD.Utilities.FVector3 rhs)

{{< /highlight >}}

Exempel

Kontrollera listan över hjälpämnen som lagts till eller uppdaterats i Wiki-dokumenten Aspose.3D:

1. [Rensar en scen i kubekartan med sex ansikten](/3d/sv/net/render-a-scene-into-the-cubemap-with-six-faces/)
1. [Rendera en Panorama vy av 3D scena](/3d/sv/net/render-a-panorama-view-of-3d-scene/)
1. [Skapa en Fisheye linseffekt på 3D scen och spara i en bild](/3d/sv/net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/)
