---
title: العام API يتغير في Aspose.3D 17.2.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Contents Sأوماري**

- [Importing Drectiles iles iles](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [يضيف Aspose.ThreeD.Formats.X.XLoadOptions Class](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

يوضح هذا المستند التغييرات إلى Aspose.3D API من الإصدار 17.1.0 إلى 17.2.0 ، والتي قد تهم مطوري الوحدات/التطبيقات. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
####  **Importing Drectiles iles iles**
Uالغناء الإصدار الأخير (17.02) أو أعلى ، يمكن للمطورين استيراد ملفات X. يتم إضافة entries he entries inary و entries exext تنسيق إدخالات لاستيراد ملفات ثنائي و ASfiles I X X.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
####  **يضيف Aspose.ThreeD.Formats.X.XLoadOptions Class**
لقد أضفنا فئة XLoadOptions. يساعد في استيراد ملفات X إلى Aspose.3D API.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// initialize Scene class object

Scene scene = new Scene();

// initialize an object

XLoadOptions loadXOpts = new XLoadOptions();

// load X file

scene.Open( "3DX.x", loadXOpts);

{{< /highlight >}}
