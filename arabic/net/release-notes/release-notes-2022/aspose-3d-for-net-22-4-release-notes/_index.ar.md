---
title: Aspose.3D for .NET 22.4 tes elease ootes
type: docs
weight: 9
url: /ar/net/aspose-3d-for-net-22-4-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D for .NET 22.4.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 22.4.

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


### Added أعضاء جدد إلى الفئة `Aspose.ThreeD.Utilities.SemanticAttribute`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Semantic of the vertex field
        /// </summary>
        public VertexFieldSemantic Semantic { get; }
        /// <summary>
        /// Alias of the vertex field
        /// </summary>
        public string Alias { get; }

        /// <summary>
        /// Initialize a <see cref="SemanticAttribute"/>
        /// </summary>
        /// <param name="semantic">The semantic of the struct's field.</param>
        /// <param name="alias">Alias of the field.</param>
        public SemanticAttribute(VertexFieldSemantic semantic, string alias)
{{< /highlight >}}

Tانه جديد وأضاف منشئ يسمح لك لتحديد الاسم المستعار لحقل فيرتكس ، والتي يمكن استخدامها لتصدير اسم الحقل المخصص في المصدرين المدعومة مثل GLTF.


### Uطريقة تاريخ AddFifield في الفئة `Aspose.ThreeD.Utilities.VertexDeclaration`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Add a new vertex field
        /// </summary>
        /// <param name="dataType">The data type of the vertex field</param>
        /// <param name="semantic">How will this field used for</param>
        /// <param name="index">The index for same field semantic</param>
        /// <param name="alias">The alias name of the field</param>
        public VertexField AddField(VertexFieldDataType dataType, VertexFieldSemantic semantic, int index = -1, string alias = null)
{{< /highlight >}}

Tانه جديد added ddFifield وأضاف بارمر جديد*الاسم المستعار*لتحديد اسم الاسم المستعار للحقل ، فإنه يعمل بالضبط نفس منشئ جديد المضافة من emanالمصنوع من ttribute.


### أعضاء Added إلى الفئة `Aspose.ThreeD.Utilities.VertexField`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Alias annotated by attribute <see cref="SemanticAttribute"/>
        /// </summary>
        public string Alias { get { return alias; } }
{{< /highlight >}}




Snقنص ode لتصدير البيانات المخصصة إلى glTF

{{< highlight "csharp" >}}

public struct Vertex
{
        [Semantic(VertexFieldSemantic.Position)]
        public FVector3 position;
        [Semantic(VertexFieldSemantic.Normal)]
        public FVector3 normal;
        [Semantic(VertexFieldSemantic.UV)]
        public FVector2 texcoord;

        //Specify the Alias of this field to "_BATCH_ID"
        [Semantic(VertexFieldSemantic.UserData, "_BATCH_ID")]
        public float batchId;

        public Vertex(FVector3 position, FVector3 normal ,FVector2 texcoord, float batchId)
        {
                this.position = position;
                this.normal = normal;
                this.texcoord = texcoord;
                this.batchId = batchId;
        }
}
private unsafe static void ExportCustomFieldToGLTF()
{
        //Prepare the vertices and indices:
        var vertices = new Vertex[]
        {
                new Vertex(new FVector3(1, 0, 0), new FVector3(0, 1, 0), new FVector2(0, 0), 1),
                new Vertex(new FVector3(1, 1, 0), new FVector3(0, 1, 0), new FVector2(0, 1), 2),
                new Vertex(new FVector3(0, 1, 0), new FVector3(0, 1, 0), new FVector2(1, 0), 3),
                new Vertex(new FVector3(0, 1, 1), new FVector3(0, 1, 0), new FVector2(1, 1), 4),
        };
        var indices = new int[]
        {
                0, 1, 2,
                1, 2, 3
        };
        //Convert the vertices into raw bytes
        var verticesInBytes = new byte[vertices.Length * sizeof(Vertex)];
        fixed(Vertex* pSrc = vertices)
        {
                Marshal.Copy(new IntPtr(pSrc), verticesInBytes, 0, vertices.Length);
        }
        //Create a vertex declaration from reflection:
        var vd = VertexDeclaration.FromType<Vertex>();
        //construct a TriMesh from raw bytes of vertices and indices
        var mesh = TriMesh.FromRawData(vd, verticesInBytes, indices, false);
        //create a scene with the mesh
        var scene = new Scene(mesh);
        //export the scene to a binary glTF file
        scene.Save("test.glb", FileFormat.GLTF2_Binary);

        // The GLTF primitive generated in the test.glb will be:
        // {"attributes" : {"POSITION" : 0, "NORMAL" : 1, "TEXCOORD_0" : 2, "_BATCH_ID" : 3}, "mode" : 4}
}



{{< /highlight >}}

