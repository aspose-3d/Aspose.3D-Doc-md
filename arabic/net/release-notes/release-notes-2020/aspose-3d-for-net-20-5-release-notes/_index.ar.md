---
title: Aspose.3D for .NET 20.5 tes elease ootes
type: docs
weight: 30
url: /ar/net/aspose-3d-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 20.5.

{{% /alert %}} 
## **Ements proو Cمعلقة**

|` `**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-664 |` `JT الملفات المستخدمة LZcompression A لا يتم دعم ضغط.|` `Enhancement|
|THREEDNET-502 |` ` Improof query query query الاستعلام ، إضافة دعم ل ateraterial/aterssetInfo/ranransform|` `Enhancement|
|THREEDNET-668 |` `Exception على تحميل DXF ملف|` `Bug|
|THREEDNET-669 |` `Export إصلاح شبكة إلى OBJ سوف تفشل|` `Bug|
|THREEDNET-670 |` ` oode. GetBh9 ingBox() قيمة خاطئة.|` `Bug|
|THREEDJAVA-73 |` `Exception على تحويل 3D ملف إلى PNG|` `Bug|
## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
- Hangشنق توقيع elecelectSingleOحقن/jecelecelecمن**Aspose.ThreeD.**



{{< highlight "java" >}}

 //public Aspose.ThreeD.A3DObject SelectSingleObject(string path)

public object SelectSingleObject(string path)

//public System.Collections.Generic.List<Aspose.ThreeD.A3DObject> SelectObjects(string path)

public System.Collections.Generic.List<object> SelectObjects(string path)

{{< /highlight >}}



**Sوافرة Code**

{{< highlight "java" >}}

 var scene = new Scene(new Torus());

foreach (BoundingBox bbox in scene.RootNode.SelectObjects("//<BoundingBox>"))

{

     Console.WriteLine($"Found a bbox : {bbox}");

}

{{< /highlight >}}

يتم تقديم Tله عن طريق THREEDNET-502 التي يمكن الاستعلام عن أشياء أعمق مثل exaterial/exexture/AssetInfo/ranransform/lements ertexE.

- Fixed مطبعي في**Aspose.ThreeD. rروفيل. HShape**



{{< highlight "java" >}}

 //Old property:

//public double OveralDepth{ get;set;}



//New property

public double OverallDepth{ get;set;} 

{{< /highlight >}}
