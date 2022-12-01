---
title: Aspose.3D for Java 19.4 tes elease ootes
type: docs
weight: 90
url: /ar/java/aspose-3d-for-java-19-4-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 19.4](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.4)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-483 |Upupport لتنسيق VRML|ميزة ew ew|
|THREEDJAVA-26|Rتقديم الدعم ل Aspose.3D for Java|ميزة ew ew|
|THREEDNET-496 |FB757500Binary inary xport ororroution sسو|Bug|

## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**

See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).

**Added الملكية الجديدة Radius في الفئة com.aspose.threed.Sphere**

{{< highlight "java" >}}

 /**

 * Gets the radius of the sphere.

 */

public double getRadius();

/**

 * Sets the radius of the sphere.

 * @param value New value

 */

public void setRadius(double value);

{{< /highlight >}}

Sرمز وافرة لتحديد دائرة نصف قطرها عن طريق الممتلكات بدلا من حجة البناء:

{{< highlight "java" >}}

 Scene scene = new Scene();

Sphere sphere = new Sphere();

sphere.setRadius(10);

scene.getRootNode().createChildNode(sphere);

scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

**Added تنسيق ملف جديد VRML في الفئة com.aspose.threed. ilileFormat و com.aspose.threed.**

{{< highlight "java" >}}

 /**

 * The Virtual Reality Modeling Language

 */

public static final FileFormat VRML;

{{< /highlight >}}

Aspose.3D يمكن الكشف التلقائي VRML تنسيق ، وبالتالي فإن FileFormat عادة ما يتم تجاهلها في طريقة القلم O. Sرمز وافرة:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.open("test.wrl");

{{< /highlight >}}
