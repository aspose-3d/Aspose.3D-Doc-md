---
title: Aspose.3D for Java 19.6 tes elease ootes
type: docs
weight: 70
url: /ar/java/aspose-3d-for-java-19-6-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 19.6](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.6)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-511|تعزيز تكوين الاسطوانة|New eature|
|THREEDNET-507|Ose نشأت بعض المواد أثناء فتح ملف RVM|Bug|
|THREEDNET-508|Tانه نظام قد تفشل في تخصيص مجموعة وصف في بعض الأحيان في renulkan renderer|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
#### **Property dded الملكية الجديدة ffffsetTop في الفئة com.aspose.threed.Cylinder**
{{< highlight "java" >}}

 /**

 * Gets the vertices transformation offset of the top side.

 */

public Vector3 getOffsetTop();

/**

 * Sets the vertices transformation offset of the top side.

 * @param value New value

 */

public void setOffsetTop(Vector3 value);

{{< /highlight >}}
#### **Added الملكية الجديدة ffffsetBorrom في الفئة com.aspose.threed.Cylinder**
{{< highlight "java" >}}

 /**

 * Gets the vertices transformation offset of the bottom side.

 */

public Vector3 getOffsetBottom();

/**

 * Sets the vertices transformation offset of the bottom side.

 * @param value New value

 */

public void setOffsetBottom(Vector3 value);

{{< /highlight >}}

Sرمز وافرة لتوليد اسطوانة مع تخصيص ffffsetTop:

{{< highlight "java" >}}

 Scene scene = new Scene();

Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

cylinder1.setOffsetTop(new Vector3(5, 3, 0));

scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);

Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

scene.getRootNode().createChildNode(cylinder2);

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

استعراض P:

![تودو: الصورة_البديل_نص](aspose-3d-for-java-19-6-release-notes_1.png)

Tترك واحد لديه**OffsetTop**تعيين إلى (5 ، 3 ، 0) ، فإنه من السهل أن نرى الغطاء العلوي قد انتقلت والجذع كله يتأثر أيضا.
#### **Property dded الملكية الجديدة enerenerateFanCylinder في الفئة com.aspose.threed.Cylinder**
{{< highlight "java" >}}

 /**

 * Gets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.

 */

public boolean getGenerateFanCylinder();

/**

 * Sets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.

 * @param value New value

 */

public void setGenerateFanCylinder(boolean value);

{{< /highlight >}}

Sرمز وافرة لتوليد اسطوانة نمط مروحة واسطوانة نمط غير مروحة:

{{< highlight "java" >}}

 Scene scene = new Scene();

Cylinder fan = new Cylinder(2, 2, 10, 20, 1, false);

fan.setGenerateFanCylinder(true);

fan.setThetaLength(MathUtils.toRadian(270.0));

scene.getRootNode().createChildNode(fan).getTransform().setTranslation(10, 0, 0);

Cylinder nonfan = new Cylinder(2, 2, 10, 20, 1, false);

scene.getRootNode().createChildNode(nonfan);

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

استعراض P:

![تودو: الصورة_البديل_نص](aspose-3d-for-java-19-6-release-notes_2.png)

Tانه ترك اسطوانة لديها enerenerateFanCylinder = كاذبة واليمين واحد لديه enerenerateFanCylinder = صحيح.
#### **Property dded عقار جديد hearhearTop في الفئة com.aspose.threed.Cylinder**
{{< highlight "java" >}}

 **

 * Gets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 */

public Vector2 getShearTop();

/**

 * Sets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 * @param value New value

 */

public void setShearTop(Vector2 value)

{{< /highlight >}}
#### **Added عقار جديد ShearBأوتوم في فئة com.aspose.threed.Cylinder**
{{< highlight "java" >}}

 /**

 * Gets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 */

public Vector2 getShearBottom();

/**

 * Sets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 * @param value New value

 */

public void setShearBottom(Vector2 value);

{{< /highlight >}}

Sرمز وافرة لإظهار استخدام hearhearBمرتفعة (ShearTop):

{{< highlight "java" >}}

 Scene scene = new Scene();

Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

cylinder1.setShearBottom(new Vector2(0, 0.83));//shear 47.5deg in xy plane(z-axis)

scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);

Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

scene.getRootNode().createChildNode(cylinder2);

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

استعراض P:

![تودو: الصورة_البديل_نص](aspose-3d-for-java-19-6-release-notes_3.png)

Tترك اسطوانة لديه hearhearBأوتوم إلى (0 ، 0.83) في حين أن الحق هو اسطوانة عادية.
