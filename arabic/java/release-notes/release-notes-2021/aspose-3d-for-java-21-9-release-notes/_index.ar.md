---
title: Aspose.3D for Java 21.9 tes elease ootes
type: docs
weight: 4
url: /ar/java/aspose-3d-for-java-21-9-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 21.9.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-930 |Add dd CD دعم التصدير|New eature|
|THREEDNET-926 |Add dd import import دعم الاستيراد|New eature|
|THREEDNET-927 |Add dd YZ دعم التصدير|New eature|
|THREEDNET-938 |Triangle المنطقة القائمة على نقطة سحابة خوارزمية توليد السطح.|New eature|
|THREEDNET-932 |Add dd oint loud دعم استيراد بصوت عال بتنسيق A3DW|New eature|
|THREEDNET-931 |Add dd oint loud دعم التصدير بصوت عال في شكل A3DW|Feature|
|THREEDNET-946 |لا يمكن تصدير oixed oointCبصوت عال إلى تنسيق PLY|إصلاح g ug|
|THREEDNET-934 |Converting من USDZ إلى OBJ نتيجة في عدم التسليم|إصلاح g ug|
|THREEDNET-936 |Contock الخلاف الناجم عن GC في FBX المستورد|حركة بلا حدود|


## API التغييرات ##


Changes ost التغييرات في 21.9 هي PointCبصوت عال ذات الصلة ، وأضاف XYZ/PCD دعم ل PointCبصوت عال ، ثابت int oint Cتصدير بصوت عال في PLY ، وأضاف PointCاستيراد بصوت عال/تصدير/تقديم الدعم في A3DW/HTML.


### Added طريقة جديدة إلى فئة com.aspose.threed. oointCبصوت عال:

{{< highlight "java" >}}
    /**
     * Create a new point cloud instance from a geometry object.
     * Density is the number of points per unit triangle(Unit triangle are the triangle with maximum surface area from the mesh)
     * @param g Mesh or other geometry instance
     * @param density Number of points per unit triangle
     */
    public static PointCloud fromGeometry(Geometry g, int density);
{{< /highlight >}}


Tانه جديد romromGeometry يسمح لك لتحديد كثافة النقاط الموزعة في مثلثات الهندسة.

Sرمز وافرة:

{{< highlight "java" >}}

        var prim = new Torus();
        var pc = PointCloud.fromGeometry(prim.toMesh(), 50);
        var s = new Scene(pc);
        s.save("point-cloud.glb", FileFormat.GLTF2_BINARY);

{{< /highlight >}}


### Added صيغ جديدة إلى الفئة com.aspose.threed. ilileFormat:

{{< highlight "java" >}}
    /**
     * Xyz point cloud file
     */
    public static final FileFormat XYZ;
    /**
     * PCL Point Cloud Data file in ASCII mode
     */
    public static final FileFormat PCD;
    /**
     * PCL Point Cloud Data file in Binary mode
     */
    public static final FileFormat PCD_BINARY;

{{< /highlight >}}


Sرمز وافرة:

{{< highlight "java" >}}

        var prim = new Torus();
        var pc = PointCloud.fromGeometry(prim.toMesh(), 50);
        var s = new Scene(pc);
        s.save("point-cloud.glb", FileFormat.PCD);

{{< /highlight >}}