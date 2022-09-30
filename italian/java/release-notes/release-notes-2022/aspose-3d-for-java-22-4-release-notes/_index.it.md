---
title: Aspose.3D for Java Note di rilascio 22.4
type: docs
weight: 9
url: /it/java/aspose-3d-for-java-22-4-release-notes/
description: Le note di rilascio dello Aspose.3D for Java 22.4.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 22.4.

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


### Aggiunto metodo AddField in classe `com.aspose.threed.VertexDeclaration`:

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

Il nuovo AddField ha aggiunto un nuovo paramter*Alias*Per specificare il nome alias del campo, funziona esattamente come il nuovo costruttore aggiunto di SemanticAttribute.


### Membri aggiunti alla classe `com.aspose.threed.VertexField`:

{{< highlight "java" >}}
    /**
     * Field's alias 
     */
    public String getAlias();

{{< /highlight >}}




Snippet di codice per esportare dati personalizzati in glTF

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

