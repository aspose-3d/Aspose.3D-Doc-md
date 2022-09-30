---
title: Aspose.3D for .NET 22,4 Utgivning
type: docs
weight: 9
url: /sv/net/aspose-3d-for-net-22-4-release-notes/
description: Publiceringsnoterna av Aspose.3D for .NET 22.4.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 22.4.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1116 |Nodes EulerAngle förvirring leder till fel position efter modellrotering|Felrättning|
|THREEDNET-1137 |LayeredTexture importerad från FBX kan skapa ogiltig GLTF-fil.|Felrättning|
|THREEDNET-1119 |Stöd för GLTF egna vertex-attribut|Ny funktion|
|THREEDNET-1129 |GLB till U3D Konvertering resulterade i fel inriktning|Ny funktion|
|THREEDNET-1121 |Exportstöd för punktmoln USD/USDZ|Ny funktion|
|THREEDNET-1122 |Stöd för punktmolnimport USD/USDZ|Ny funktion|
|THREEDNET-1113 |Laddad OBJ modell förlorade konsistenskoordinater vt|Felrättning|
|THREEDNET-1107 |Licensen kan inte laddas när programmet byggs som en enda körbarhet.|Felrättning|


## API ändringar ##


Alla API ändringar i denna version behövs för att exportera användardata glTF till `TriMesh`, användardata i `Mesh` och `VertexElementUserData` stöds i nästa version.


### Lagt till nya medlemmar i klass `Aspose.ThreeD.Utilities.SemanticAttribute`:

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

Den nya tillagda konstruktorn låter dig ange ett alias för vertexfältet, som kan användas för att exportera anpassade fältnamn i stödda exportörer som GLTF.


### Uppdateringsmetod AddField i klass `Aspose.ThreeD.Utilities.VertexDeclaration`:

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

Den nya AddField lade till en ny paramter*Alias*För att ange fältets aliasnamn, fungerar det exakt samma som den nya tillagda konstruktören av SemanticAttribute.


### Medlemmar till `Aspose.ThreeD.Utilities.VertexField`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Alias annotated by attribute <see cref="SemanticAttribute"/>
        /// </summary>
        public string Alias { get { return alias; } }
{{< /highlight >}}




Kod snutt för att exportera egna data till glTF

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

