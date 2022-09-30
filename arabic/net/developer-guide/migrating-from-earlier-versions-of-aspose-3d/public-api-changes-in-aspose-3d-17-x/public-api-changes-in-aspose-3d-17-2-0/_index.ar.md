---
title: Hangublic API hangمعلقة في Aspose.3D 17.2.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Contents Sأوماري**

- [Importing DirectX iles iles](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Adds Aspose.ThreeD. orormat. X. Xptions oadOptions lass](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 17.1.0 إلى 17.2.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
#### **Importing DirectX iles iles**
Uالغناء الإصدار الأخير (17.02) أو أعلى ، يمكن للمطورين استيراد ملفات X. يتم إضافة entries he entries inary و entries exext تنسيق إدخالات لاستيراد الملفات الثنائية و ASCII X.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Adds Aspose.ThreeD. orormat. X. Xptions oadOptions lass**
لقد أضاف We فئة ptions ptions oadO. It يساعد في استيراد ملفات X إلى Aspose.3D API.

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
