---
title: Hangublic API hangمعلقة في Aspose.3D 16.12.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Contents Sأوماري**

- [Adds Aspose.ThreeD. tered tered lass](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Importing DXF iles](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 16.11.0 إلى 16.12.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Adds Aspose.ThreeD. tered tered lass**
A طريقة لتطبيق رخصة المقننة.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
### **Importing DXF iles**
Uالغناء الإصدار الأخير (16.12.0) أو أعلى ، يمكن للمطورين استيراد الملفات DXF. يتم إضافة إدخال تنسيق he he DXF لأغراض التحميل.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
