---
title: Aspose.3D for .NET 19.8 tes elease ootes
type: docs
weight: 50
url: /ar/net/aspose-3d-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.8](/3d/ar/net/aspose-3d-for-net-19-8-release-notes/)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-528|Add نقطة دعم سحابة في Wavefront OBJ|New eature|
|THREEDNET-531|Sمراجعة الشوائب من Aspose.3D|Enhancement|
|THREEDNET-536 |DRC إلى STL فشل التحويل|Bug|
|THREEDNET-537|Problem تحويل PLY إلى GLB|Bug|
|THREEDNET-539|Tانه سحابة نقطة كبيرة قد تولد بيانات غير صحيحة|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **Property dded خاصية جديدة oointCبصوت عال في الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

/// </summary>

public bool PointCloud

{

    get;set;

}

{{< /highlight >}}

Sرمز وافرة لتوليد سحابة نقطة من ere phere في شكل obj.

{{< highlight "java" >}}

 var scene = new Scene(new Sphere());

scene.Save(@"sphere.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
### **Added طرق جديدة CreatePأوليغون Aspose.ThreeD. nntities. Msh**
{{< highlight "java" >}}

 /// <summary>

/// Create a polygon with 4 vertices(quad)

/// </summary>

/// <param name="v1">Index of the first vertex</param>

/// <param name="v2">Index of the second vertex</param>

/// <param name="v3">Index of the third vertex</param>

/// <param name="v4">Index of the fourth vertex</param>

public void CreatePolygon(int v1, int v2, int v3, int v4);

/// <summary>

/// Create a polygon with 3 vertices(triangle)

/// </summary>

/// <param name="v1">Index of the first vertex</param>

/// <param name="v2">Index of the second vertex</param>

/// <param name="v3">Index of the third vertex</param>

public void CreatePolygon(int v1, int v2, int v3);

{{< /highlight >}}

Sرمز وافرة.

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

mesh.CreatePolygon(new int[]{ 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices

mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

{{< /highlight >}}

Tوأضاف أساليب جديدة**CreatePأوليغون**تسمح لك بإنشاء مثلث أو رباعية دون تخصيص ذاكرة إضافية ، انها الأمثل للغاية داخليا.


### **Rالرموز التعبيرية الحقل العام القديم rerettyPrint في الفئة Aspose.ThreeD. orormat. ptions ptions ptions ptions aveOptions**
Tتمت إزالة له واستبدالها الممتلكات مع نفس الاسم ، لذلك رمز القديمة التي تستخدم هذا لا يحتاج إلى تعديلات.
### **Property dded خاصية جديدة rerettyPrint في الفئة Aspose.ThreeD. orormat. ptions ptions ptions ptions aveOptions**

{{< highlight "java" >}}

 /// <summary>

/// The JSON content of GLTF file is indented for human reading, default value is false

/// </summary>

public bool PrettyPrint { get; set; }

{{< /highlight >}}

Tانه قديم**PrettyPrint**كان حقل عام ، وتم استبداله بالممتلكات بشكل ثابت.
