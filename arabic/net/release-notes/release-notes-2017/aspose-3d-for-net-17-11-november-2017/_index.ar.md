---
title: Aspose.3D for .NET 17.11-Nنوفمبر 2017
type: docs
weight: 20
url: /ar/net/aspose-3d-for-net-17-11-november-2017/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.11](https://www.nuget.org/packages/Aspose.3D/17.11.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-303|Add دعم استيراد RVM-ثنائي (AVEVA 07MS S)|ميزة ew ew|
|THREEDNET-305|Add دعم شبكات الاندماج|ميزة ew ew|
|THREEDNET-306|FBX إلى GLTF-تعتيم المواد غير صحيحة في GLTF|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Members dds RvmText و RvmBالبولي أعضاء إلى Aspose.ThreeD.FileFormat الفئة**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// AVEVA Plant Design Management System Model in text format

/// </summary>

public static readonly FileFormat RvmText;

/// <summary>

/// AVEVA Plant Design Management System Model in binary format

/// </summary>

public static readonly FileFormat RvmBinary;

{{< /highlight >}}

يتم دعم Auto تنسيق الكشف عن ملف PD0707RVM ، لذلك يمكن للمطورين استيراده مباشرة مع منشئ فئة cencene دون تحديد صراحة orileFormat.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene("stablizer.rvm");

{{< /highlight >}}

{{% alert color="primary" %}} 

Tانه البدائية في الملفات RVM سيتم تحويلها إلى تنسجم أثناء الاستيراد.

{{% /alert %}}
#### **Adds Aspose.ThreeD. orormat. class vmLoadOفئة الوصفات**
The خصائص egylinderRadialSegments ، يتم استخدام مساحيق ishishLongtalldements ، مساحيق ishishLatitudeSو مساحيق orusTubularSللتحكم في طريقة تحويل البدائية المحددة في ملفات Rvm إلى شبكات. يمكن العثور على tails etails في الطبقات Aspose.ThreeD. nntities. Cylinder و Aspose.ThreeD. nntities. ororus

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Load options for AVEVA Plant Design Management System's RVM file.

/// </summary>

public class RvmLoadOptions : LoadOptions

{

    /// <summary>

    /// The RVM file contains no material information, but the Aspose.3D can generate materials for each objects.

    /// Default value is true

    /// </summary>

    public bool GenerateMaterials { get; set; }

    /// <summary>

    /// Gets or sets the number of cylinder's radial segments, default value is 16

    /// </summary>

    public int CylinderRadialSegments { get; set; }

    /// <summary>

    /// Gets or sets the number of dish's longitude segments, default value is 12

    /// </summary>

    public int DishLongitudeSegments { get; set; }

    /// <summary>

    /// Gets or sets the number of dish's latitude segments, default value is 8 

    /// </summary>

    public int DishLatitudeSegments { get; set; }

    /// <summary>

    /// Gets or sets the number of torus's tubular segments, default value is 20 

    /// </summary>

    public int TorusTubularSegments { get; set; }

    /// <summary>

    /// Construct a <see cref="RvmLoadOptions"/> instance

    /// </summary>

    /// <param name="contentType"></param>

    public RvmLoadOptions(FileContentType contentType);

    /// <summary>

    /// Construct a <see cref="RvmLoadOptions"/> instance

    /// </summary>

    public RvmLoadOptions();

}

{{< /highlight >}}

**Sرمز وافرة:**

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

scene.Open("LAD-TOP.rvm", opt);

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **يتم إضافة 3 أعضاء في Aspose.ThreeD. nntities.**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Convert a whole node to a single transformed mesh

/// Vertex elements like normal/texture coordinates are not supported yet

/// </summary>

/// <param name="node">The node to merge</param>

/// <returns>Merged mesh</returns>

public static Mesh MergeMesh(Node node)

/// <summary>

/// Convert a whole scene to a single transformed mesh

/// Vertex elements like normal/texture coordinates are not supported yet

/// </summary>

/// <param name="scene">The scene to merge</param>

/// <returns>The merged mesh</returns>

public static Mesh MergeMesh(Scene scene);

/// <summary>

/// Convert a whole node to a single transformed mesh

/// Vertex elements like normal/texture coordinates are not supported yet

/// </summary>

/// <param name="nodes">The nodes to merge</param>

/// <returns>Merged mesh</returns>

public static Mesh MergeMesh(IList<Node> nodes);

{{< /highlight >}}

**Sرمز وافرة:**

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene("LAD-TOP.rvm");

Mesh mesh = PolygonModifier.MergeMesh(scene);

FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

{{< /highlight >}}
#### **يتم إضافة عضو رانسبارنسي 07إلى Aspose.ThreeD.Shading.PbrMaterial الفئة**
Only GLTF 2.0 يدعم المواد PBR ، لذلك يؤثر هذا التحسن فقط على تصدير GLTF 2.0.

**C#**

{{< highlight "java" >}}

 /// <summary>

///  Gets or sets the transparency factor.

/// The factor should be ranged between 0(0%, fully opaque) and 1(100%, fully transparent)

/// Any invalid factor value will be clamped.

/// </summary>

/// <value>The transparency factor.</value>

public double Transparency { get; set; }

{{< /highlight >}}

**Sرمز وافرة:**

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("box", new Box()).Material = new PbrMaterial() {Transparency = 0.5, Albedo = new Vector3(Color.AliceBlue)};

scene.Save("box.gltf", FileFormat.GLTF2);

{{< /highlight >}}
#### **Uحكيم Examles**
Pالإيجار تحقق من قائمة المواضيع المساعدة المضافة أو updated في مستندات Aspose.3D Wiki:

1. [في 3D ملف](/3d/ar/net/merge-meshes-in-3d-file/)
1. [Use RVM خيارات التحميل](/3d/ar/net/specify-3d-file-load-options/#specify3dfileloadoptions-uservmloadoptions)
