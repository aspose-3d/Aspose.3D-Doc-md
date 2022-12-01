---
title: Aspose.3D for .NET 17.6 tes elease ootes
type: docs
weight: 70
url: /ar/net/aspose-3d-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.6](https://www.nuget.org/packages/Aspose.3D/17.6.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-257|Export 3D المشهد إلى GLTF 2.0 ASCII الملفات|ميزة ew ew|
|THREEDNET-258|Export 3D المشهد إلى GLTF 2.0 الملفات البولي B|ميزة ew ew|
|THREEDNET-264|Models لديه الظل ولكن ليس لديه ثنائية العادية لن تجعل بشكل صحيح|Bug|
|THREEDNET-267|المواد Mفي Collada الملفات قد لا يتم تحميلها بشكل صحيح.|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Adds ateraterialConverter ember إلى Aspose.ThreeD**
GLTF 2.0 يدعم فقط مواد PBR ، Aspose.3D سوف يحول داخليا المواد غير PBR إلى مواد PBقبل التصدير إلى GLTF 2.0 (المواد في المشهد ستبقى دون تغيير أثناء التصدير) ، ويمكن للمستخدم توفير وظيفة تحويل مخصصة لتجاوز السلوك الافتراضي.

Tمثال التعليمات البرمجية له يوضح كيفية تحويل المواد إلى المواد PBR ، ومن ثم توفير 3D المشهد إلى GLTF 2.0 تنسيق:

**.NET, C#**

{{< highlight "java" >}}

 var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

s.Save("test.gltf", opt);

{{< /highlight >}}
### **Uحكيم Examles**
Pالإيجار تحقق من قائمة المواضيع المساعدة المضافة أو updated في مستندات Aspose.3D Wiki:

1. [Customize Non-PBR إلى aterateraterالمواد ononقبل aving aving 3D cencenإلى GLTF 2.0 orormat](/3d/ar/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/)
