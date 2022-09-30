---
title: Aspose.3D for .NET 17.3.0 tes elease ootes
type: docs
weight: 100
url: /ar/net/aspose-3d-for-net-17-3-0-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.3.0](https://www.nuget.org/packages/Aspose.3D/17.3.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-233|Add دعم استيراد ملفات Google Draco (.drc).|ميزة ew ew|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Adds Draco تنسيق الدخول في Aspose.ThreeD.FileFormat lass**
Tالإفراج عنه من Aspose.3D for .NET API قد أضاف دعم استيراد Google Draco(.drc) الملفات. Dإيفليرز يمكن استيراد ملف Google Draco ، ومن ثم حفظه في أي تنسيق 3D المدعومة.

Tمثال رمزه يوضح كيفية استيراد ملف Google Draco إلى Aspose.3D API:

**.NET, C#**

{{< highlight "java" >}}

 // Initialize a Scene class object

Scene scene = new Scene();

// load an existing 3D document

scene.Open("document.drc", FileFormat.Draco);

{{< /highlight >}}
