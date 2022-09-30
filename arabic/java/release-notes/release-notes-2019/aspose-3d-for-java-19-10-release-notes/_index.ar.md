---
title: Aspose.3D for Java 19.10 tes elease ootes
type: docs
weight: 30
url: /ar/java/aspose-3d-for-java-19-10-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 19.10](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.10).

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-567 |` `Problem تحويل RVM و ATT البلاط|` `Enhancement|
|THREEDNET-570 |` ` حساب غير صحيح من صندوق الحدود من الأشكال البدائية غير صحيحة|` `Enhancement|
|THREEDNET-571 |` `Export الأشكال البدائية إلى ملف RVM.|` `Enhancement|
|THREEDNET-572 |` ` دعم التصدير البدائي في FBX.|` `Enhancement|
|THREEDNET-573 |` ` لا يمكن تصدير الرسوم البيانية في اسم الكائن بشكل صحيح بتنسيق FBX|` `Bug|
|THREEDNET-568 |` `Saved. لا يمكن فتح ملفات glb.|` `Bug|
|THREEDNET-549|Loading ضخمة RVM يأخذ الكثير من الوقت والموارد|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **New Class - com.aspose.threed. ish ish**
Tله هو شكل بدائي جديد.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish", new Dish(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **New Cلاس كوم. aspose.threed. ramyramid**
Tله هو شكل بدائي جديد.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("pyramid", new Pyramid(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **خصائص ew ew تضاف إلى الفئة com.aspose.threed. ox ox**


Tتم إضافة الخصائص التالية إلى Aspose.ThreeD. nntities. Box الفئة.

{{< highlight "java" >}}

 /**

\* Gets the length segments.

*/

public int getLengthSegments();

/**

\* Sets the length segments.

\* @param value New value

*/

public void setLengthSegments(int value);

/**

\* Gets the width segments

*/

public int getWidthSegments();

/**

\* Sets the width segments

\* @param value New value

*/

public void setWidthSegments(int value);

/**

\* gets or sets the height segments.

*/

public int getHeightSegments();

/**

\* gets or sets the height segments.

\* @param value New value

*/

public void setHeightSegments(int value);

{{< /highlight >}}
### **Rطريقة عاطفية FindNode في الفئة com.aspose.threed. oode**
Tكان من المقرر إزالتها منذ أن تم استبدالها من قبل أكثر تقدما elecelectSingleOحقن/jecelectOالقاذفات.
### **طريقة ew ew تضاف إلى الفئة com.aspose.threed. oode**
Tتم إضافة الطريقة التالية إلى Aspose.ThreeD.Node الفئة مما يجعلها أكثر ملاءمة لإنشاء عقدة مع المواد المضادة للأشعة فوق البنفسجية.

{{< highlight "java" >}}

 /**

\* Create a new child node with given node name, and attach specified entity and a material

\* @param nodeName The new child node's name

\* @param entity Default entity attached to the node

\* @param material The material attached to the node

\* @return The new child node.

*/

public Node createChildNode(String nodeName, Entity entity, Material material);

{{< /highlight >}}

Sرمز وافرة

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish", new Box(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **طرق المشاعر Rمن الفئة com.aspose.threed. lylyFormat**


Tتم استبدال الطرق التالية من قبل PlyFormat.Encode التي يمكن أيضا أن تستخدم لترميز سحابة نقطة.



{{< highlight "java" >}}

 private void encodeMesh(IMeshConvertible mesh, Stream stream, PlySaveOptions opt) throws IOException;

private void encodeMesh(IMeshConvertible mesh, String fileName, PlySaveOptions opt) throws IOException;

{{< /highlight >}}
### **Added عقار جديد إلى الفئة com.aspose.threed. Fptions ptions ptions**
Tممتلكاته يجعل من المفيد تصدير المشاهد الكبيرة التي تتكون من البدائية.



{{< highlight "java" >}}

 /**

 * Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

\* Default value is false

*/

public boolean getReusePrimitiveMesh();



/**

\* Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

\* Default value is false

\* @param value New value

*/

public void setReusePrimitiveMesh(boolean value);

{{< /highlight >}}
#### **Sوافرة Code**
{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish A", new Dish(), new PbrMaterial(Color.blue));

scene.getRootNode().createChildNode("dish B", new Dish(), new PbrMaterial(Color.blue));

FBXSaveOptions opt = new FBXSaveOptions(FileFormat.FBX7400ASCII);

opt.setReusePrimitiveMesh(true);

scene.save("file.fbx", opt);

{{< /highlight >}}



Since اثنين من الأشكال parameterized لديها نفس المعلمات ، وأنها سوف تولد بالتأكيد نفس الشبكة. When هذه الخاصية صحيحة ، فإن ملف FBX الذي تم إنشاؤه سيولد شبكة واحدة فقط ويعيد استخدامه في العقد المختلفة.
