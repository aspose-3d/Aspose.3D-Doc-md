---
title: Aspose.3D for .NET 19.9 tes elease ootes
type: docs
weight: 40
url: /ar/net/aspose-3d-for-net-19-9-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.9](/3d/ar/net/aspose-3d-for-net-19-9-release-notes/)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-532|Export 3D مشهد إلى HTML|New eature|
|THREEDNET-561|Expose خصائص التحول الهندسي|Enhancement|
|THREEDNET-556|يبدو دوران مقياس الحرارة غير صحيح|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **Added تنسيقات الملفات الجديدة HTML5/Aspose3 Deb eb**
{{< highlight "java" >}}

 /// <summary>

/// Aspose.3D Web format.

/// </summary>

public static readonly FileFormat Aspose3DWeb;

/// <summary>

/// HTML5 File

/// </summary>

public static readonly FileFormat HTML5;

{{< /highlight >}}

When تقوم بتصدير المشهد إلى ملف HTML5 ، سيكون هناك في الواقع 3 ملفات ، ملف HTML ، ملف Aspose3 eb eb eb (*.a3dw) ، وملف كريبت rendered avaSالمقدمة ، يمكنك فقط تصدير ملف a3dw عن طريق تحديد Aspose3 Deb eb كنوع التصدير ، وإعادة استخدام ملف جافا سكريبت داخل الصفحة الخاصة بك HTML.

Sرمز وافرة:

{{< highlight "java" >}}

 var scene = new Scene();

var node = scene.RootNode.CreateChildNode(new Cylinder());

node.Material = new LambertMaterial() { DiffuseColor = new Vector3(Color.Chartreuse) };

scene.RootNode.CreateChildNode(new Light() { LightType = LightType.Point }).Transform.Translation = new Vector3(10, 0, 10);

scene.Save(@"test.html", FileFormat.HTML5);

{{< /highlight >}}

{{% alert color="primary" %}} 

Due إلى الحدود الأمنية للمتصفح ، لا يمكن فتح ملف HTML المصدرة مباشرة ، تحتاج إلى فتحه من خلال خادم ويب ، إذا كان لديك python3 مثبت ، يمكنك بدء تشغيل خادم الويب في سطر الأوامر في الدليل المصدرة

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Tالدجاجة فتحه<http://localhost:8000/test.html>. The يستخدم بائع الويب ebebGL2 ، يمكنك استخدام<https://get.webgl.org/webgl2/>للتحقق مما إذا كان المتصفح يدعم ذلك أم لا.
### **Added فئة جديدة Aspose.ThreeD. orormat. HTptions ptions 5SaveOptions**
Tله يسمح لك لتخصيص تصدير 3D HTML صفحة

Sرمز وافرة:

{{< highlight "java" >}}

 var scene = new Scene();

var node = scene.RootNode.CreateChildNode(new Cylinder());

node.Material = new LambertMaterial() { DiffuseColor = new Vector3(Color.Chartreuse) };

scene.RootNode.CreateChildNode(new Light() { LightType = LightType.Point }).Transform.Translation = new Vector3(10, 0, 10);

var opt = new HTML5SaveOptions();

opt.ShowGrid = false;  //Turn off the grid

opt.ShowUI = false; //Turn off the user interface.

scene.Save(@"test.html", opt);

{{< /highlight >}}
### **Property dded الملكية الجديدة FileFormat في الفئة Aspose.ThreeD. orormat. IOononfig**
{{< highlight "java" >}}

 /// <summary>

/// Gets the file format that specified in current Save/Load option.

/// </summary>

public FileFormat FileFormat { get; }

{{< /highlight >}}
### **Added طريقة جديدة EvaluateGlobalTransform في الفئة Aspose.ThreeD. oode**
{{< highlight "java" >}}

 /// <summary>

/// Evaluate the global transform, include the geometric transform or not.

/// </summary>

/// <param name="withGeometricTransform">Whether the geometric transform is needed.</param>

/// <returns></returns>

public Matrix4 EvaluateGlobalTransform(bool withGeometricTransform);

{{< /highlight >}}

Tانه الفرق بين oode. lolobalTransform. ranransformMatrix هو أنه يسمح لك للحصول على مصفوفة التحول مع تحويل هندسي ، مما يؤثر فقط على الكيان المرفق ويحافظ على العقد الطفل غير متأثرة.
### **Added خصائص جديدة caleometricTranslation/الترسبات eometricS/ الترسبات eometricRفي الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the geometric translation. 

/// Geometric transformation only affects the entities attached and leave the child nodes unaffected.

/// It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

/// </summary>

public Vector3 GeometricTranslation {get; set;}

/// <summary>

/// Gets or sets the geometric scaling. 

/// Geometric transformation only affects the entities attached and leave the child nodes unaffected.

/// It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

/// </summary>

public Vector3 GeometricScaling {get; set;}

/// <summary>

/// Gets or sets the geometric euler rotation(measured in degree). 

/// Geometric transformation only affects the entities attached and leave the child nodes unaffected.

/// It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

/// </summary>

public Vector3 GeometricRotation {get; set; }

{{< /highlight >}}

Sرمز وافرة:

{{< highlight "java" >}}

 var n = new Node();

n.Transform.GeometricTranslation = new Vector3(10, 0, 0);

Console.WriteLine(n.EvaluateGlobalTransform(true));

Console.WriteLine(n.EvaluateGlobalTransform(false));

{{< /highlight >}}

Tانه أول Cononly. Wريتو سيخرج من مصفوفة التحويل التي تشمل التحول الهندسي في حين أن الثاني لن.
