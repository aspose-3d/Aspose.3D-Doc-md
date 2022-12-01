---
title: Aspose.3D for .NET 19.10 tes elease ootes
type: docs
weight: 30
url: /ar/net/aspose-3d-for-net-19-10-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الافراج عن Aspose.3D for .NET 19.10.

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-567 |` `Problem تحويل RVM و ATT البلاط|Enhancement|
|THREEDNET-570 |` ` حساب غير صحيح من صندوق الحدود من الأشكال البدائية غير صحيحة|Enhancement|
|THREEDNET-571 |` `Export الأشكال البدائية إلى ملف RVM.|Enhancement|
|THREEDNET-572 |` ` دعم التصدير البدائي في FBX.|Enhancement|
|THREEDNET-573 |` ` لا يمكن تصدير الرسوم البيانية في اسم الكائن بشكل صحيح بتنسيق FBX|Bug|
|THREEDNET-568 |` `Saved. لا يمكن فتح ملفات glb.|Bug|
|THREEDNET-549|Loading ضخمة RVM يأخذ الكثير من الوقت والموارد|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **New lass لاس-Aspose.ThreeD. nntities. Dish**
Tله هو شكل بدائي جديد.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("dish", new Dish(), new PbrMaterial(Color.Coral));

{{< /highlight >}}
### **New lass las-Aspose.ThreeD. nntities. Pyramid**
Tله هو شكل بدائي جديد.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("pyramid", new Pyramid(), new PbrMaterial(Color.Coral));

{{< /highlight >}}
### **خصائص ew ew تضاف إلى الفئة Aspose.ThreeD. nntities. ox ox**


Tتم إضافة الخصائص التالية إلى Aspose.ThreeD. nntities. Box الفئة.

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the length segments.

/// </summary>

public int LengthSegments{ get;set;}

/// <summary>

/// Gets or sets the width segments

/// </summary>

public int WidthSegments{ get;set;}

/// <summary>

/// gets or sets the height segments.

/// </summary>

public int HeightSegments{ get;set;}

{{< /highlight >}}
### **Rطريقة الرموز التعبيرية في الفئة Aspose.ThreeD.**
Tكان من المقرر إزالتها منذ أن تم استبدالها من قبل أكثر تقدما elecelectSingleOحقن/jecelectOالقاذفات.
### **طريقة ew ew المضافة إلى الفئة Aspose.ThreeD.**
Tتم إضافة الطريقة التالية إلى Aspose.ThreeD.Node الفئة مما يجعلها أكثر ملاءمة لإنشاء عقدة مع المواد المضادة للأشعة فوق البنفسجية.

{{< highlight "java" >}}

 /// <summary>

/// Create a new child node with given node name, and attach specified entity and a material

/// </summary>

/// <param name="nodeName">The new child node's name</param>

/// <param name="entity">Default entity attached to the node</param>

/// <param name="material">The material attached to the node</param>

/// <returns>The new child node.</returns>

public Node CreateChildNode(string nodeName, Entity entity, Material material);

{{< /highlight >}}

Sرمز وافرة

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("box", new Box(), new PbrMaterial(Color.Coral));

{{< /highlight >}}

طرق الرموز التعبيرية من الفئة Aspose.ThreeD. orormat. PlyFormat

Tتم استبدال الطرق التالية من قبل PlyFormat.Encode التي يمكن أيضا أن تستخدم لترميز سحابة نقطة.



{{< highlight "java" >}}

 public void EncodeMesh(Aspose.ThreeD.Entities.IMeshConvertible mesh, System.IO.Stream stream, Aspose.ThreeD.Formats.PlySaveOptions opt);

public void EncodeMesh(Aspose.ThreeD.Entities.IMeshConvertible mesh, string fileName, Aspose.ThreeD.Formats.PlySaveOptions opt);

{{< /highlight >}}

Added خاصية جديدة إلى الفئة Aspose.ThreeD. orormat. ptions ptions ptions ptions

Tممتلكاته يجعل من المفيد تصدير المشاهد الكبيرة التي تتكون من البدائية.



{{< highlight "java" >}}

 /// <summary>

/// Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

/// Default value is false

/// </summary>

public bool ReusePrimitiveMesh { get; set; }

{{< /highlight >}}
#### **Sوافرة Code**
{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("dish A", new Dish(), new PbrMaterial(Color.Coral));

scene.RootNode.CreateChildNode("dish B", new Dish(), new PbrMaterial(Color.Coral));

scene.Save("file.fbx", new FBXSaveOptions(FileFormat.FBX7400ASCII) { ReusePrimitiveMesh = true });

{{< /highlight >}}



Since اثنين من الأشكال parameterized لديها نفس المعلمات ، وأنها سوف تولد بالتأكيد نفس الشبكة. When هذه الخاصية صحيحة ، فإن ملف FBX الذي تم إنشاؤه سيولد شبكة واحدة فقط ويعيد استخدامه في العقد المختلفة.
