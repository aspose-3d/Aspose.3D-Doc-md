---
title: Aspose.3D for .NET 18.10-أكتوبر 2018
type: docs
weight: 30
url: /ar/net/aspose-3d-for-net-18-10-october-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 18.10](https://www.nuget.org/packages/Aspose.3D/18.10.0).

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-434|Support for .NET منصة خام C|New eature|
|THREEDNET-431|Allow المستخدم لإيقاف الضغط عند توفير FBX الملفات الثنائية|New eature|
|THREEDNET-424|Import mproof FBX أداء الاستيراد|Enhancement|
|THREEDNET-432|Improof FBX أداء الكتابة البولي|Enhancement|
|THREEDNET-428|ImportException أثناء فتح ملفات ضخمة FBX|Bug|
|THREEDNET-429|Problem مع property nitScaleFخاصية الممثل|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **API التغييرات**
#### **أعضاء Added إلى الفئة Aspose.ThreeD. orormat. ptions ptions ptions ptions aveOptions:**
{{< highlight "java" >}}

         /// <summary>

        /// Compression large binary data in the FBX file, default value is true.

        /// </summary>

        public bool EnableCompression{ get;set;}

{{< /highlight >}}

**Sوافرة oode:**

{{< highlight "java" >}}

         Scene scene = new Scene("test.fbx");

        scene.Save("test.fbx", new FBXSaveOptions(FileFormat.FBX7500ASCII) {EnableCompression = false});

{{< /highlight >}}
