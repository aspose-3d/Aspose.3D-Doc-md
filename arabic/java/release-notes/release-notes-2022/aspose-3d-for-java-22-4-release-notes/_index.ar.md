---
title: Aspose.3D for Java 22.4 tes elease ootes
type: docs
weight: 9
url: /ar/java/aspose-3d-for-java-22-4-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D for Java 22.4.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 22.4.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1116 |Confusion ode's EulerAngle confusion يؤدي إلى وضع خاطئ بعد دوران النموذج|إصلاح g ug|
|THREEDNET-1137 |LayeredTexture المستوردة من FBX قد تولد ملف غير صالح GLTF|إصلاح g ug|
|THREEDNET-1119 |Upupport ل GLTF Custom Vertex ttttributes|New eature|
|THREEDNET-1129 |GLB إلى U3D أدى الاتجاه غير الصحيح|New eature|
|THREEDNET-1121 |دعم الصادرات السحابية من Point في USD/USDZ|New eature|
|THREEDNET-1122 |Pدعم استيراد سحابة oint في USD/USDZ|New eature|
|THREEDNET-1113 |Loading OBJ نموذج فقدت نسيج إحداثيات vt|إصلاح g ug|
|THREEDNET-1107 |Tلا يمكن تحميل الترخيص عندما يتم بناء التطبيق باعتباره قابل للتنفيذ واحد.|إصلاح g ug|


## API التغييرات ##


All API هناك حاجة إلى تغييرات في هذا الإصدار لتصدير بيانات المستخدم في glTF من خلال `TriMesh` ، سيتم دعم بيانات المستخدم في `Mesh` و `VertexElementUserData` في الإصدار التالي.


### طريقة ded dded في الفئة `com.aspose.threed.VertexDeclaration`:

{{< highlight "java" >}}
    /**
     * Add a new vertex field
     * @param dataType The data type of the vertex field
     * @param semantic How will this field used for
     * @param index The index for same field semantic, -1 for auto-generation
     * @param alias The alias name of the field
     */
    public VertexField addField(int dataType, VertexFieldSemantic semantic, int index, String alias);

{{< /highlight >}}

Tانه جديد added ddFifield وأضاف بارمر جديد*الاسم المستعار*لتحديد اسم الاسم المستعار للحقل ، فإنه يعمل بالضبط نفس منشئ جديد المضافة من emanالمصنوع من ttribute.


### أعضاء Added إلى الفئة `com.aspose.threed.VertexField`:

{{< highlight "java" >}}
    /**
     * Field's alias 
     */
    public String getAlias();

{{< /highlight >}}




Snقنص ode لتصدير البيانات المخصصة إلى glTF

{{< highlight "java" >}}

private static void writeVertex(DataOutputStream writer,
                                float px, float py, float pz,
                                float nx, float ny, float nz,
                                float u, float v,
                                float batchId)
        throws IOException
{
        writer.writeFloat(px);
        writer.writeFloat(py);
        writer.writeFloat(pz);

        writer.writeFloat(nx);
        writer.writeFloat(ny);
        writer.writeFloat(nz);

        writer.writeFloat(u);
        writer.writeFloat(v);

        writer.writeFloat(batchId);
}

private static void exportCustomFieldToGLTF()
        throws Exception
{
        byte[] verticesInBytes;
        try(var os = new ByteArrayOutputStream())
        {
            try(var writer = new DataOutputStream(os)) {
                writeVertex(writer, 1, 0, 0, 0, 1, 0, 0, 0, 1);
                writeVertex(writer, 1, 1, 0, 0, 1, 0, 0, 1, 2);
                writeVertex(writer, 0, 1, 0, 0, 1, 0, 1, 0, 3);
                writeVertex(writer, 0, 1, 1, 0, 1, 0, 1, 1, 4);
            }
            verticesInBytes = os.toByteArray();
        }
        var indices = new int[]
        {
                0, 1, 2,
                1, 2, 3
        };
        //create a vertex declaration
        VertexDeclaration vd = new VertexDeclaration();
        vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.POSITION);
        vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
        vd.addField(VertexFieldDataType.F_VECTOR2, VertexFieldSemantic.UV);
        vd.addField(VertexFieldDataType.FLOAT, VertexFieldSemantic.USER_DATA, -1, "_BATCH_ID");
        //construct a TriMesh from raw bytes of vertices and indices
        var mesh = TriMesh.fromRawData(vd, verticesInBytes, indices, false);
        //create a scene with the mesh
        var scene = new Scene(mesh);
        //export the scene to a binary glTF file
        scene.save("test.glb", FileFormat.GLTF2_BINARY);
        // The GLTF primitive generated in the test.glb will be:
        // {"attributes" : {"POSITION" : 1, "NORMAL" : 3, "TEXCOORD_0" : 2, "_BATCH_ID" : 4}, "mode" : 4}
}



{{< /highlight >}}

