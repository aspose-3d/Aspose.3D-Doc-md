---
title: Aspose.3D for .NET 17.5 tes elease ootes
type: docs
weight: 80
url: /ar/net/aspose-3d-for-net-17-5-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.5](https://www.nuget.org/packages/Aspose.3D/17.5.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-244|New ew material R المواد لدعم تقديم القائمة جسديا|ميزة ew ew|
|THREEDNET-250|Allow Aspose.3D API لاستيراد GLTF 2.0 ASCII الملفات|ميزة ew ew|
|THREEDNET-253|Allow Aspose.3D API لاستيراد GLTF 2.0 ملف البولي|ميزة ew ew|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Adds Aspose.ThreeD. hhading. PbrMaterial lass**
Tلقد أضاف الإصدار الأخير من Aspose.3D for .NET API دعم PBR (Pبشكل hysally ased en) المواد. Dإيفليرز يمكن تطبيق المواد PBR إلى الكيانات وتقديم في نماذج 3D.

Tمثال التعليمات البرمجية له يوضح كيفية تطبيق المواد PPR على كيان:

**.NET, C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

PbrMaterial mat = new PbrMaterial();

mat.MetallicFactor = 0.9;//an almost metal material

mat.RoughnessFactor = 0.9;//material surface is very rough

//create a box that applied this material

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

{{< /highlight >}}
#### **تحديثات ember ember إلى Aspose.ThreeD. lass ileFormat lass**
Added o استيراد GLTF 2.0 (ASCII و inary inary) الملفات إلى Aspose.3D API ، يتم إضافة عضوين (GLT2 2 & GL22 _ inary inary) إلى Aspose.ThreeD.

Tمثال code يوضح كيفية استيراد GLTF 2.0 ASCII أو الملف البولي B:

**.NET, C#**

{{< highlight "java" >}}

 /********************** New Members **********************/

public static readonly Aspose.ThreeD.FileFormat GLTF2;

public static readonly Aspose.ThreeD.FileFormat GLTF2_Binary;



/******************** Import GLTF 2.0 ********************/

//Create a new scene

var s = new Scene();

//Load it as GLTF2, the second argument is optional since Aspose.3D can detect the actual file type

s.Open("test.gltf", FileFormat.GLTF2);

{{< /highlight >}}

