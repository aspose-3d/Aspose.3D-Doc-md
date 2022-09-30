---
title: Aspose.3D for .NET 17.8 tes elease ootes
type: docs
weight: 50
url: /ar/net/aspose-3d-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.8](https://www.nuget.org/packages/Aspose.3D/17.8.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-279|مشهد ender ender في خريطة مكعب مع 6 وجوه.|ميزة ew ew|
|THREEDNET-280|Add بعد معالجة الإسقاط إكويرتريل.|ميزة ew ew|
|THREEDNET-281|Render مكعب خريطة إلى عين السمكة.|ميزة ew ew|
|THREEDNET-276|تحويل غير صحيح من OBJ إلى GLTF و GLB.|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **يمكن إزالة الثوالب التي تم وضع علامة عليها باسم obsoleted وسيتم إزالتها في نهاية هذا العام 2017**
يتم تمثيل 17.8 جميع وحدات الملمس (المستخدمة من قبل بائع) من قبل واجهة IexextureUnit ولكن هذا التصميم لا يعمل بشكل جيد لخريطة مكعب والملمس 3D في المستقبل (لم تنفذ بعد) ، لذلك يتم وضع علامة على هذه الأساليب كلها كما عفا عليها الزمن ، للتأكد من أن التعليمات البرمجية لن كسر مترجم ، يجب على المطورين استخدام الأساليب مع نفس الاسم من Iexexture1D/Iexexture2D/IexextureCubemap.

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
#### **Added جديد enum نوع Aspose.ThreeD. ender اندر. CubeFace**
Ttype يعمل مع Aspose.ThreeD. Rاندر. CubeFaceData<>و Aspose.ThreeD. Rاندر. IexextureCubemap للوصول إلى البيانات وفقا لوجه cubemap.

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
#### **Added فئة جديدة Aspose.ThreeD. ender اندر. CubeFaceData<>**
Tفئته هي فئة عامة لوصف كل بيانات الوجه cubemap مثل اسم الملف أو bitmap.
#### **Added فئة جديدة Aspose.ThreeD. ender اندر. exexextureCubemap**
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
#### **Added فئة جديدة Aspose.ThreeD. ender اندر. Iexexture1D**
يستخدم Tواجهة له لتمثيل كائن الملمس 1D
#### **Added فئة جديدة Aspose.ThreeD. ender اندر. Iexexture2D**
يستخدم Tواجهة له لتمثيل كائن نسيج 2D
#### **Added طرق جديدة إلى الفئة Aspose.ThreeD.**
**C#**

{{< highlight "java" >}}

 // this is an overloaded version for method IRenderTexture CreateRenderTexture(Aspose.ThreeD.Render.RenderParameters parameters, int targets, int width, int height) with targets to 1

public Aspose.ThreeD.Render.IRenderTexture CreteRenderTexture(Aspose.ThreeD.Render.RenderParameters parameters, int width, int height)

//Create a render target that will render the scene into a cube map

public Aspose.ThreeD.Render.IRenderTexture CreateCubeRenderTexture(Aspose.ThreeD.Render.RenderParameters parameters, int width, int height)

// allow user to create ITexture1D/ITexture2D/ITextureCubemap manually

public Aspose.ThreeD.Render.ITextureUnit CreateTextureUnit(Aspose.ThreeD.Render.TextureType textureType)

{{< /highlight >}}
#### **Added طريقة جديدة في الفئة Aspose.ThreeD. ender اندر. enenderer:**
In الإصدارات السابقة يمكن استخدام معالجة البريد فقط من خلال توفير سلسلة من تأثيرات معالجة البريد إلى Aspose.ThreeD.Render.Renderer. يمكن للمستخدم الآن مع هذا الأسلوب تنفيذ إجراء معالجة آخر يدويا ، وهذا مفيد في ميزة جديدة THREEDNET-280 THREEDNET-281 ، يعني أنه يمكنك تقديم خريطة cubemap إلى صورة بانوراما أو صورة عين السمكة.

**C#**

{{< highlight "java" >}}

 public void Execute(Aspose.ThreeD.Render.PostProcessing postProcessing, Aspose.ThreeD.Render.IRenderTarget result)

{{< /highlight >}}






#### **Enerنشيط ananorama Image في 3D cencene**
يمكن استخدام أدوات الطرف 3rd مثل three.js/js ano2VR لتصور النتيجة.

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







**Generate ishisheye ens ens ffffect in 3D cencene**

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

**طرق Added لهيكلة Aspose.ThreeD. tilitulties. Fecector3:**

These هما العمليتان البدائيتان للناقلات.

**C#**

{{< highlight "java" >}}

 //Calculate the normalized vector of the FVector3, equivalent implementation of Vector3.Normalize

public Aspose.ThreeD.Utilities.FVector3 Normalize()

//Calculate the cross product of two FVector3, equivalent implementation of Vector3.Cross

public Aspose.ThreeD.Utilities.FVector3 Cross(Aspose.ThreeD.Utilities.FVector3 rhs)

{{< /highlight >}}

Uحكيم Examles

Pالإيجار تحقق من قائمة المواضيع المساعدة المضافة أو updated في مستندات Aspose.3D Wiki:

1. [Render مشهد في cubemap مع ستة وجوه](/3d/ar/net/render-a-scene-into-the-cubemap-with-six-faces/)
1. [Rأندر وجهة نظر أنوراما من 3D المشهد](/3d/ar/net/render-a-panorama-view-of-3d-scene/)
1. [Create تأثير عدسة ishisheye على 3D المشهد وحفظ في صورة](/3d/ar/net/create-a-fisheye-lens-effect-on-3d-scene-and-save-in-an-image/)
