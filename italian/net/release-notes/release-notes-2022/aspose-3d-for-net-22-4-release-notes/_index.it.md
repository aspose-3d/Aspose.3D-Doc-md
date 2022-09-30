---
title: Aspose.3D for .NET Note di rilascio 22.4
type: docs
weight: 9
url: /it/net/aspose-3d-for-net-22-4-release-notes/
description: Le note di rilascio dello Aspose.3D for .NET 22.4.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 22.4.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1116 |La confusione di EulerAngle del nodo porta a una posizione sbagliata dopo la rotazione del modello|Correzione di bug|
|THREEDNET-1137 |LayeredTexture importato dallo FBX può generare file GLTF non validi|Correzione di bug|
|THREEDNET-1119 |Supporto per gli attributi Vertex personalizzati GLTF|Nuova funzione|
|THREEDNET-1129 |GLB a U3D La conversione ha provocato un orientamento sbagliato|Nuova funzione|
|THREEDNET-1121 |Supporto per l'esportazione di cloud point nel numero USD/USDZ|Nuova funzione|
|THREEDNET-1122 |Supporto per l'importazione di cloud point nel numero USD/USDZ|Nuova funzione|
|THREEDNET-1113 |Caricato OBJ modello perso texture coordinate vt|Correzione di bug|
|THREEDNET-1107 |La licenza non può essere caricata quando l'applicazione viene costruita come un singolo eseguibile.|Correzione di bug|


## API modifiche ##


Tutte le modifiche API in questa versione sono necessarie per esportare i dati dell'utente negli glTF agli `TriMesh`, i dati utente negli `Mesh` e `VertexElementUserData` saranno supportati nella prossima versione.


### Aggiunti nuovi membri alla classe `Aspose.ThreeD.Utilities.SemanticAttribute`:

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

Il nuovo costruttore aggiunto consente di specificare un alias per il campo vertice, che può essere utilizzato per esportare il nome del campo personalizzato in esportatori supportati come GLTF.


### Metodo di aggiornamento AddField in classe `Aspose.ThreeD.Utilities.VertexDeclaration`:

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

Il nuovo AddField ha aggiunto un nuovo paramter*Alias*Per specificare il nome alias del campo, funziona esattamente come il nuovo costruttore aggiunto di SemanticAttribute.


### Membri aggiunti alla classe `Aspose.ThreeD.Utilities.VertexField`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Alias annotated by attribute <see cref="SemanticAttribute"/>
        /// </summary>
        public string Alias { get { return alias; } }
{{< /highlight >}}




Snippet di codice per esportare dati personalizzati in glTF

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

