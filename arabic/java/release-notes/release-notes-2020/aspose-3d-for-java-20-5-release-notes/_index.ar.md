---
title: Aspose.3D for Java 20.5 tes elease ootes
type: docs
weight: 30
url: /ar/java/aspose-3d-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 20.5.

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
## **Hangublic API و ackackward hangمتوافق مع hangمعلقة**
- Hangشنق توقيع elecelectSingleOحقن/jecelecelecمن**كوم. أسبوس. ثريد.**



{{< highlight "java" >}}

 //public java.util.ArrayList<com.aspose.threed.A3DObject> com.aspose.threed.Node.selectObjects(java.lang.String) throws com.aspose.threed.ParseException;

public java.util.ArrayList<java.lang.Object> com.aspose.threed.Node.selectObjects(java.lang.String) throws com.aspose.threed.ParseException;

//public com.aspose.threed.A3DObject com.aspose.threed.Node.selectSingleObject(java.lang.String) throws com.aspose.threed.ParseException;

public java.lang.Object com.aspose.threed.Node.selectSingleObject(java.lang.String) throws com.aspose.threed.ParseException;

{{< /highlight >}}


**Sوافرة Code**

{{< highlight "java" >}}

 Scene scene = new Scene(new Torus());

for(Object bbox : scene.getRootNode().selectObjects("//<BoundingBox>"))

{

     System.out.printf("Found a bbox : %s\n", bbox);

}

{{< /highlight >}}

يتم تقديم Tله عن طريق THREEDNET-502 التي يمكن الاستعلام عن أشياء أعمق مثل exaterial/exexture/AssetInfo/ranransform/lements ertexE.

- Fixed مطبعي في com.a**Spose. threed. spoShape**



{{< highlight "java" >}}

 //public void com.aspose.threed.HShape.setOveralDepth(double);

public void com.aspose.threed.HShape.setOverallDepth(double);

//public double com.aspose.threed.HShape.getOveralDepth();

public double com.aspose.threed.HShape.getOverallDepth();

{{< /highlight >}}
