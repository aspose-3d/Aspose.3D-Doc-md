---
title: API العام يتغير بـ Aspose.3D 16.12.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Contents Sأوماري**

- [تضيف Aspose.ThreeD.Metered Class](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [استيراد ملفات DXF](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

يوضح هذا المستند التغييرات إلى Aspose.3D API من الإصدار 16.11.0 إلى 16.12.0 ، والتي قد تهم مطوري الوحدات/التطبيقات. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **تضيف Aspose.ThreeD.Metered Class**
A طريقة لتطبيق رخصة المقننة.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
###  **استيراد ملفات DXF**
باستخدام الإصدار الأخير (16.12.0) أو أعلى ، يمكن للمطورين استيراد ملفات DXF. تمت إضافة إدخال تنسيق DXF لأغراض التحميل.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
