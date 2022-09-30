---
title: Public API hangمعلقة في Aspose.3D 1.1.0
type: docs
weight: 60
url: /ar/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Contents Sأوماري**

- [يتم إضافة FBX7200ASCaving aving aving ption ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [يتم إضافة ption BX7200Binary aving ption ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [يتم إضافة FBX7300ASCaving aving aving ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [يتم إضافة ption BX7300Binary aving ption ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [WavefrontOBJ يتم إضافة ption aving ption في orileFormat و ilileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 1.0.0 إلى 1.1.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **يتم إضافة FBX7200ASCaving aving aving ption ption في orileFormat**
تم إضافة خيار تنسيق Fhe he he X7200ASformat في FileFormat enum. It يمثل ASCII FBX تنسيق الملف ، مع إصدار 7.2.0. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **يتم إضافة ption BX7200Binary aving ption ption في orileFormat**
تم إضافة الخيار inary he he B7200Bتنسيق البولي في orileFormat enum. It يمثل تنسيق ملف البولي FBX ، مع إصدار 7.2.0. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **يتم إضافة FBX7300ASCaving aving aving ption في orileFormat**
تم إضافة خيار تنسيق Fhe he he 77300ASformat في FileFormat enum. It يمثل ASCII FBX تنسيق الملف ، مع إصدار 7.3.0. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **يتم إضافة ption BX7300Binary aving ption ption في orileFormat**
تم إضافة الخيار inary he he B7300Bتنسيق البولي في orileFormat enum. It يمثل تنسيق ملف البولي FBX ، مع إصدار 7.3.0. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **WavefrontOBJ يتم إضافة ption aving ption في orileFormat و ilileFormatType**
تم إضافة خيار تنسيق he he WavefrontOBJ في orileFormat و ilileFormatType enams. It يمثل Wavefront تنسيق ملف Obj. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

