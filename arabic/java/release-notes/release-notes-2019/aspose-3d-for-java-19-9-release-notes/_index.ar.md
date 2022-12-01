---
title: Aspose.3D for Java 19.9 tes elease ootes
type: docs
weight: 40
url: /ar/java/aspose-3d-for-java-19-9-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الافراج عن Aspose.3D for Java 19.9

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-532|Export 3D مشهد إلى HTML|New eature|
|THREEDNET-561|Expose خصائص التحول الهندسي|Enhancement|
|THREEDNET-556|يبدو دوران مقياس الحرارة غير صحيح|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **Formats dded تنسيقات الملفات الجديدة HTML5/ASPOSE3D_WEB**
{{< highlight "java" >}}

 /**

\* Aspose.3D Web format.

*/

public static final FileFormat ASPOSE3D_WEB;

/**

\* HTML5 File

*/

public static final FileFormat HTML5;

{{< /highlight >}}

When تقوم بتصدير المشهد إلى ملف HTML5 ، سيكون هناك في الواقع 3 ملفات ، ملف HTML ، ملف Aspose3 eb eb eb (*.a3dw) ، وملف كريبت rendered avaSالمقدمة ، يمكنك فقط تصدير ملف a3dw عن طريق تحديد Aspose3 Deb eb كنوع التصدير ، وإعادة استخدام ملف جافا سكريبت داخل الصفحة الخاصة بك HTML.

Sرمز وافرة:

{{< highlight "java" >}}

 Scene scene = new Scene();

Node node = scene.getRootNode().createChildNode(new Cylinder());

LambertMaterial mat = new LambertMaterial();

mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));

node.setMaterial(mat);

Light light = new Light();

light.setLightType(LightType.POINT);

scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);

scene.save("test.html", FileFormat.HTML5);

{{< /highlight >}}

{{% alert color="primary" %}} 

Due إلى الحدود الأمنية للمتصفح ، لا يمكن فتح ملف HTML المصدرة مباشرة ، تحتاج إلى فتحه من خلال خادم ويب ، إذا كان لديك python3 مثبت ، يمكنك بدء تشغيل خادم الويب في سطر الأوامر في الدليل المصدرة

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Tالدجاجة فتحه**http:// localيقبل: 8000/test .html**. The يستخدم بائع الويب ebebGL2 ، يمكنك استخدام<https://get.webgl.org/webgl2/>للتحقق مما إذا كان المتصفح يدعم ذلك أم لا.
### **Added فئة جديدة com.aspose.threed. Hptions ptions ptions 5SaveOptions**
Tله يسمح لك لتخصيص تصدير 3D HTML صفحة

Sرمز وافرة:

{{< highlight "java" >}}

 Scene scene = new Scene();

Node node = scene.getRootNode().createChildNode(new Cylinder());

LambertMaterial mat = new LambertMaterial();

mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));

node.setMaterial(mat);

Light light = new Light();

light.setLightType(LightType.POINT);

scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);

HTML5SaveOptions opt = new HTML5SaveOptions();

opt.setShowGrid(false); // Turn off the grid

opt.setShowUI(false); //Turn off the user interface

scene.save("test.html", FileFormat.HTML5);

{{< /highlight >}}
### **Added الملكية الجديدة FileFormat في الفئة com.aspose.threed. Iononfig**
{{< highlight "java" >}}

 /**

 * Gets the file format that specified in current Save/Load option.

 */

public FileFormat getFileFormat();

{{< /highlight >}}
### **Added طريقة جديدة evaluateGlobalTransform في الفئة com.aspose.threed. oode**
{{< highlight "java" >}}

 /**

 * Evaluate the global transform, include the geometric transform or not.

 * @param withGeometricTransform Whether the geometric transform is needed.

 */

public Matrix4 evaluateGlobalTransform(boolean withGeometricTransform);

{{< /highlight >}}

Tانه الفرق بين oode. lolobalTransform. ranransformMatrix هو أنه يسمح لك للحصول على مصفوفة التحول مع تحويل هندسي ، مما يؤثر فقط على الكيان المرفق ويحافظ على العقد الطفل غير متأثرة.
### **Added جديد getter/اضع gettriceometricranranslation**


{{< highlight "java" >}}

 /**

 * Gets the geometric translation.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 */

public Vector3 getGeometricTranslation();

/**

 * Sets the geometric translation.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 * @param value New value

 */

public void setGeometricTranslation(Vector3 value);

/**

 * Gets the geometric scaling.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 */

public Vector3 getGeometricScaling();

/**

 * Sets the geometric scaling.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 * @param value New value

 */

public void setGeometricScaling(Vector3 value);

/**

 * Gets the geometric euler rotation(measured in degree).

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 */

public Vector3 getGeometricRotation();

/**

 * Sets the geometric euler rotation(measured in degree).

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 * @param value New value

 */

public void setGeometricRotation(Vector3 value);

{{< /highlight >}}



Sرمز وافرة:

{{< highlight "java" >}}

 Node n = new Node();

n.getTransform().setGeometricTranslation(new Vector3(10, 0, 0));

System.out.println(n.evaluateGlobalTransform(true));

System.out.println(n.evaluateGlobalTransform(false));

{{< /highlight >}}

Tانه أول بيان الطباعة سوف إخراج مصفوفة التحويل التي تشمل التحول الهندسي في حين أن الثاني لن.
