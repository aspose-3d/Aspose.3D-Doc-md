---
title: Aspose.3D for Java 19.5 tes elease ootes
type: docs
weight: 80
url: /ar/java/aspose-3d-for-java-19-5-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 19.5](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.5)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-501|Iteمع أحدث ynynabic. tered tered|Enhancement|
|THREEDNET-505|Aانخفاض اتجاه طائرة التغيير عن طريق تحديد ما يصل العادي|Enhancement|
|THREEDNET-489|Shadow لا يعمل في renulkan renderer|Bug|
|THREEDNET-504|Draco تم إنشاؤه من STL يتم كسر الملف|Bug|

## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).

**Added عقار جديد * Radius * في الفئة com.aspose.threed. lane lane**

{{< highlight "java" >}}

 /**

 * Gets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

 */

public Vector3 getUp();

/**

 * Sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

 * @param value New value

 */

public void setUp(Vector3 value);

{{< /highlight >}}

Sرمز وافرة لتحديد دائرة نصف قطرها عن طريق الممتلكات بدلا من حجة البناء:

{{< highlight "java" >}}

 Scene scene = new Scene();

Plane plane = new Plane();

plane.setUp(new Vector3(1, 1, 3));

scene.getRootNode().createChildNode(plane);

//This will generate a plane that has customized orientation

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

**Added طريقة جديدة "getConsumptionCريديت" في الفئة com.aspose.threed. tered**

{{< highlight "java" >}}

 /**

\* Gets consumption credit

\* @return consumption quantity

*/

public static double getConsumptionCredit() throws Exception;

{{< /highlight >}}

Ets ets الائتمان الاستهلاك من الشهر الحالي ، وتستخدم من قبل Dynabic. Mخدمة الفواتير المقننة.
