---
title: Aspose.3D for Java 22,4 Utgivning
type: docs
weight: 9
url: /sv/java/aspose-3d-for-java-22-4-release-notes/
description: Publiceringsnoterna av Aspose.3D for Java 22.4.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 22.4.

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


### AddField i klass `com.aspose.threed.VertexDeclaration`:

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

Den nya AddField lade till en ny paramter*Alias*För att ange fältets aliasnamn, fungerar det exakt samma som den nya tillagda konstruktören av SemanticAttribute.


### Medlemmar till `com.aspose.threed.VertexField`:

{{< highlight "java" >}}
    /**
     * Field's alias 
     */
    public String getAlias();

{{< /highlight >}}




Kod snutt för att exportera egna data till glTF

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

