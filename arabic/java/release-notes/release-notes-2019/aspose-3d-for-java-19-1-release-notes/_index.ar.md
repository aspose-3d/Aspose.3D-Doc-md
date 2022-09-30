---
title: Aspose.3D for Java 19.1 tes elease ootes
type: docs
weight: 120
url: /ar/java/aspose-3d-for-java-19-1-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الافراج عن Aspose.3D for Java 19.1.

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Sأوماري**|**Category**|
|:- |:- |
|Uatlas أطلس خوارزمية|New eature|
|AMF زابورتر|New eature|
|كشف تنسيق الملف القائم على Archive|New eature|

## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).

**Added فئة com.aspose.threed. Aptions ptions aveOptions:**

{{< highlight "java" >}}

 /**

 * Save options for AMF

 */

public class AMFSaveOptions extends SaveOptions

{ 



    /**

     * Whether to use compression to reduce the final file size, default value is true

     */

    public boolean getEnableCompression();



    /**

     * Whether to use compression to reduce the final file size, default value is true

     * @param value New value

     */

    public void setEnableCompression(boolean value);

}

{{< /highlight >}}

**وأضاف عضو ew ew إلى فئة 'com.aspose.threed. olyأوليغونستر أوديفير':**

{{< highlight "java" >}}

     /**

     * Generate UV data from the given input mesh and specified normal data.

     * @param mesh The input mesh

     * @param normals The normal data

     * @return Generated UV data

     */

    public static VertexElementUV generateUV(Mesh mesh, VertexElementNormal normals);

    /**

     * Generate UV data from the given input mesh

     * @param mesh The input mesh

     * @return Generated UV data

     */

    public static VertexElementUV generateUV(Mesh mesh);

{{< /highlight >}}




