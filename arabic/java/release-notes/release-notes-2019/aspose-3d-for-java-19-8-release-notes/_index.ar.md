---
title: Aspose.3D for Java 19.8 tes elease ootes
type: docs
weight: 50
url: /ar/java/aspose-3d-for-java-19-8-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 19.8](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.8)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-528|Add نقطة دعم سحابة في Wavefront OBJ|New eature|
|THREEDNET-531|Sمراجعة الشوائب من Aspose.3D|Enhancement|
|THREEDNET-536 |DRC إلى STL فشل التحويل|Bug|
|THREEDNET-537|Problem تحويل PLY إلى GLB|Bug|
|THREEDNET-539|Tانه سحابة نقطة كبيرة قد تولد بيانات غير صحيحة|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **Added جديد getter/setter oointCبصوت عال في الفئة com.aspose.threed.**
{{< highlight "java" >}}

 /**

 * Gets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

 */

public boolean getPointCloud();

/**

 * Sets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

 * @param value New value

 */

public void setPointCloud(boolean value);

{{< /highlight >}}

Sرمز وافرة لتوليد سحابة نقطة من ere phere في شكل obj.

{{< highlight "java" >}}

 Scene scene = new Scene(new Sphere());

ObjSaveOptions opt = new ObjSaveOptions();

opt.setPointCloud(true);

scene.save("sphere.obj", opt);

{{< /highlight >}}
### **Added طرق جديدة createPأوليغون com.aspose.threed. esh sh**
{{< highlight "java" >}}

 /**

 * Create a polygon with 4 vertices(quad)

 * @param v1 Index of the first vertex

 * @param v2 Index of the second vertex

 * @param v3 Index of the third vertex

 * @param v4 Index of the fourth vertex

 */

public void createPolygon(int v1, int v2, int v3, int v4);

/**

 * Create a polygon with 3 vertices(triangle)

 * @param v1 Index of the first vertex

 * @param v2 Index of the second vertex

 * @param v3 Index of the third vertex

 */

public void createPolygon(int v1, int v2, int v3);

{{< /highlight >}}

Sرمز وافرة.

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

mesh.createPolygon(new int[]{ 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices

mesh.createPolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

{{< /highlight >}}

Tوأضاف أساليب جديدة**CreatePأوليغون**تسمح لك بإنشاء مثلث أو رباعية دون تخصيص ذاكرة إضافية ، انها الأمثل للغاية داخليا.


### **Rالرموز التعبيرية الحقل العام القديم prettyPrint في الفئة com.aspose.threed. ptions ptions ptions ptions aveOptions**
Tتمت إزالة له واستبدالها الممتلكات مع نفس الاسم.
### **Ptions dded جديد getter/اضع rerettyPrint في الفئة com.aspose.threed.**
{{< highlight "java" >}}

 /**

\* The JSON content of GLTF file is indented for human reading, default value is false

*/

public boolean getPrettyPrint();

/**

\* The JSON content of GLTF file is indented for human reading, default value is false

\* @param value New value

*/

public void setPrettyPrint(boolean value);

{{< /highlight >}}

Tانه قديم**بريتي رينت**كان حقل عام ، وتم استبداله بالممتلكات بشكل ثابت.

Sوافرة oode.

{{< highlight "java" >}}

 Scene scene = new Scene(new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//opt.prettyPrint = true; //Old code

opt.setPrettyPrint(true); //Use setter to change this configuration.

scene.save("sphere.gltf", opt);

{{< /highlight >}}




