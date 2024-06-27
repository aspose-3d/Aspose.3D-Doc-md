---
title: العام API يتغير بـ Aspose.3D 1.1.0
type: docs
weight: 60
url: /ar/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Contents Sأوماري**

- [يتم إضافة FBX7200ASCaving aving aving ption ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [يتم إضافة ption BX7200Binary aving ption ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [يتم إضافة FBX7300ASCaving aving aving ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [يتم إضافة ption BX7300Binary aving ption ption في orileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [تمت إضافة خيار التوفير WavefrontOBJ بتنسيق الملف ونوع الملف](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

توضح هذه الوثيقة التغييرات إلى Aspose.3D API من الإصدار 1.0.0 إلى 1.1.0 ، والتي قد تهم مطوري الوحدات/التطبيقات. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **يتم إضافة FBX7200ASCaving aving aving ption ption في orileFormat**
تمت إضافة خيار تنسيق FBX7200ASCII في قائمة الملفات. يمثل تنسيق ملف ASCII FBX ، مع إصدار 7.2.0. رمز المثال:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

###  **يتم إضافة ption BX7200Binary aving ption ption في orileFormat**
تمت إضافة خيار تنسيق FBX7200Binary في قائمة الملفات. إنه يمثل تنسيق ملف FBX ثنائي ، مع إصدار 7.2.0. رمز المثال:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

###  **يتم إضافة FBX7300ASCaving aving aving ption في orileFormat**
تمت إضافة خيار تنسيق FBX7300ASCII في قائمة الملفات. إنه يمثل تنسيق ملف ASCII FBX ، مع إصدار 7.3.0. رمز المثال:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

###  **يتم إضافة ption BX7300Binary aving ption ption في orileFormat**
تمت إضافة خيار تنسيق FBX7300Binary في الشمول. يمثل تنسيق الملف الثنائي FBX ، مع إصدار 7.3.0. رمز المثال:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

###  **تمت إضافة خيار التوفير WavefrontOBJ بتنسيق الملف ونوع الملف**
تمت إضافة خيار التنسيق WavefrontOBJ في تنسيقات الملفات وتعداد FileFormatType. يمثل تنسيق ملف Obj Wavefront. رمز المثال:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

