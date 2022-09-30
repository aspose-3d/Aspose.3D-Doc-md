---
title: Aspose.3D for .NET 17.12-Dديسمبر 2017
type: docs
weight: 10
url: /ar/net/aspose-3d-for-net-17-12-december-2017/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.12](https://www.nuget.org/packages/Aspose.3D/17.12.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-304|Add دعم تصدير RVM (AVdd dd A 0707S S)|ميزة ew ew|
|THREEDNET-312|Add طريقة قصيرة لقياس الهندسة|حركة بلا حدود|
|THREEDNET-314|Add دعم تصدير الممتلكات المخصصة/ID إلى العقد في شكل GLTF|حركة بلا حدود|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Property dds property aveExtras خاصية إلى Aspose.ThreeD. ororالحصير. class orproperty class class aveOptions الفئة**
Tهو القيمة الافتراضية للخاصية avaveExtras كاذبة ، إذا كنت تريد Aspose.3D for .NET API لتصدير خصائص مخصصة للكائن ، يمكنك تعيينه إلى صحيح.

**C#**

{{< highlight "java" >}}

 public bool SaveExtras{ get;set;}

{{< /highlight >}}

{{% alert color="primary" %}} 

سيتم حفظ خصائص مخصصة في حقل "خارج" بسبب مواصفات glTF. يتم سرد المثال رمز A أدناه.

{{% /alert %}}
#### **Adds ثلاثة أعضاء إلى Aspose.ThreeD. A3Dclass فئة حقن**
EmoemoveProperty ، GetProperty ، SetProperty هي مجموعة من طرق قصيرة اليد لمعالجة خصائص مخصصة للكائن. Tانه الأساليب القديمة مثل FindProperty و rereateDynamicProperty هي verbose جدا ، ومن المقرر إزالتها في المستقبل. Tيتم دعم خصائص مخصصة من قبل FBX/glTF (إصدارات ll ll).

**C#**

{{< highlight "java" >}}

 public bool RemoveProperty(string property)

public object GetProperty(string property)

public void SetProperty(string property, object value)

{{< /highlight >}}

**Sرمز وافرة:**

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

var box = scene.RootNode.CreateChildNode("box", new Box());

box.SetProperty("obj-id", "box-id");

scene.Save("test.fbx", FileFormat.FBX7400ASCII);

scene.Save("test.gltf", new GLTFSaveOptions(FileFormat.GLTF){SaveExtras = true});

scene.Save("test-2.gltf", new GLTFSaveOptions(FileFormat.GLTF2){SaveExtras = true});

{{< /highlight >}}

Tله رمز العينة سوف ينقذ المشهد مع خصائص مخصصة إلى FBX ، glTF و glTF 2.0.
#### **Adds اثنين من الأعضاء إلى Aspose.ThreeD.**
أعضاء ese hese في متناول اليد ، إذا كان المطورين لا يريدون تغيير تحويل العقدة ولكنهم يرغبون في توسيع نطاق الهندسة وينطبق فقط على الهندسة.

**C#**

{{< highlight "java" >}}

 public static void Scale(Aspose.ThreeD.Scene scene, Aspose.ThreeD.Utilities.Vector3 scale)

public static void Scale(Aspose.ThreeD.Node node, Aspose.ThreeD.Utilities.Vector3 scale)

{{< /highlight >}}

**Sرمز وافرة:**

**C#**

{{< highlight "java" >}}

 // scale the model in huge-scene.obj by 0.01 and save it to another file:

Scene scene = new Scene("huge-scene.obj");

PolygonModifier.Scale(scene, new Vector3(0.01));

scene.Save("scaled-scene.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Adds indindNطريقة ode إلى Aspose.ThreeD.**
Tله هو طريقة مفيدة للعثور على عقدة الطفل بالاسم ، وسوف يعود لاغية إذا لم تتمكن من العثور على عقدة.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("child", new Box());

Node child = scene.RootNode.FindNode("child");

{{< /highlight >}}
#### **Uحكيم Examles**
Pالإيجار تحقق من قائمة المواضيع المساعدة المضافة أو updated في مستندات Aspose.3D Wiki:

1. [Mخصائص مخصصة من 3D cenسين](/3d/ar/net/manipulate-custom-properties-of-a-3d-scene/)
1. [Scale هندسي من 3D cencene](/3d/ar/net/scale-geometries-of-a-3d-scene/)
