---
title: Aspose.3D for .NET 19.7 tes elease ootes
type: docs
weight: 60
url: /ar/net/aspose-3d-for-net-19-7-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.7](https://www.nuget.org/packages/Aspose.3D/19.7.0)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-449|Roroblem مع قيم التحول في oodes|Feature|
|THREEDNET-526|Add نقطة دعم التصدير سحابة في Google Draco|Enhancement|
|THREEDNET-524|Add نقطة دعم استيراد سحابة في Google Draco|Enhancement|
|THREEDNET-523 |دعم سحابة نقطة dd dd بتنسيق PLY|Enhancement|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **Added فئة جديدة Aspose.ThreeD. nntities. oointCبصوت عال**
Tصفته يرث من Aspose.ThreeD. nntities. omeeometry مباشرة وتستخدم لتمثيل مجموعة من النقاط.
### **Added طرق جديدة ecoecode إلى الفئة Aspose.ThreeD. orormat. racracoFormat**
{{< highlight "java" >}}

 /// <summary>

/// Decode the point cloud or mesh from specified file name

/// </summary>

/// <param name="fileName">The file name contains the drc file</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance depends on the file content</returns>

public Geometry Decode(string fileName);

/// <summary>

/// Decode the point cloud or mesh from memory data

/// </summary>

/// <param name="data">The raw drc bytes</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance depends on the content</returns>

public Geometry Decode(byte[]data)

{{< /highlight >}}

Sرمز وافرة لفك تشفير شبكة من ملف دراكو مباشرة دون بناء مشهد

{{< highlight "java" >}}

 var pointCloud = (PointCloud) FileFormat.Draco.Decode("pointCloud.drc");

{{< /highlight >}}
### **Added طرق جديدة Encode إلى الفئة Aspose.ThreeD. orormat. racracoForma**
{{< highlight "java" >}}

 /// <summary>

/// Encode the entity to specified stream

/// </summary>

/// <param name="entity">The entity to be encoded</param>

/// <param name="stream">The stream that encoded data will be written to</param>

/// <param name="options">Extra options for encoding the point cloud</param>

public void Encode(Entity entity, Stream stream, DracoSaveOptions options = null);

/// <summary>

/// Encode the entity to specified file

/// </summary>

/// <param name="entity">The entity to be encoded</param>

/// <param name="fileName">The file name to be written</param>

/// <param name="options">Extra options for encoding the point cloud</param>

public void Encode(Entity entity, string fileName, DracoSaveOptions options = null);

/// <summary>

/// Encode the entity to Draco raw data

/// </summary>

/// <param name="entity">The entity to be encoded</param>

/// <param name="options">Extra options for encoding the point cloud</param>

/// <returns>The encoded draco data represented in bytes</returns>

public byte[]Encode(Entity entity, DracoSaveOptions options = null);

{{< /highlight >}}

Sرمز وافرة لترميز شبكة المجال لملف دراكو مباشرة دون بناء مشهد

{{< highlight "java" >}}

 FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
### **Added طرق جديدة oointCبصوت عال إلى الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

 /// <summary>

/// Export the scene as point cloud, default value is false.

/// </summary>

public bool PointCloud { get; set; } 

{{< /highlight >}}

Sرمز وافرة لترميز شبكة المجال إلى ملف دراكو كسحابة نقطة

{{< highlight "java" >}}

 FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() {PointCloud = true});

{{< /highlight >}}
### **Added طرق جديدة Encode إلى الفئة Aspose.ThreeD. orormat. PlyFormat**
{{< highlight "java" >}}

 /// <summary>

/// Encode the entity and save the result into the stream.

/// </summary>

/// <param name="entity">The entity to encode</param>

/// <param name="stream">The stream to write to, this method will not close this stream</param>

/// <param name="opt">Save options</param>

public void Encode(Entity entity, Stream stream, PlySaveOptions opt = null);

/// <summary>

/// Encode the entity and save the result into an external file.

/// </summary>

/// <param name="entity">The entity to encode</param>

/// <param name="fileName">The file to write to</param>

/// <param name="opt">Save options</param>

public void Encode(Entity entity, string fileName, PlySaveOptions opt = null);

{{< /highlight >}}

Sرمز وافرة لترميز شبكة لملف رقائق مباشرة دون بناء مشهد.

{{< highlight "java" >}}

 FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
### **Added طرق جديدة ecoecode إلى الفئة Aspose.ThreeD. orormat. PlyFormat**
{{< highlight "java" >}}

 /// <summary>

/// Decode a point cloud or mesh from the specified stream.

/// </summary>

/// <param name="fileName">The input stream</param>

/// <param name="opt">The load option of PLY format</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance</returns>

public Geometry Decode(string fileName, PlyLoadOptions opt = null);

/// <summary>

/// Decode a point cloud or mesh from the specified stream.

/// </summary>

/// <param name="stream">The input stream</param>

/// <param name="opt">The load option of PLY format</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance</returns>

public Geometry Decode(Stream stream, PlyLoadOptions opt = null);

{{< /highlight >}}

Sرمز وافرة لفك تشفير سحابة شبكة/نقطة من ملف رقائق:

{{< highlight "java" >}}

 var geom = FileFormat.PLY.Decode("sphere.ply");

{{< /highlight >}}
### **Property dded الملكية PointCبصوت عال إلى الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

 /// <summary>

/// Export the scene as point cloud, the default value is false.

/// </summary>

public bool PointCloud { get; set; }

{{< /highlight >}}

Sرمز وافرة لإجبار تصدير مشهد إلى رقائق كسحابة نقطة

{{< highlight "java" >}}

 FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions(){PointCloud = true});

{{< /highlight >}}
