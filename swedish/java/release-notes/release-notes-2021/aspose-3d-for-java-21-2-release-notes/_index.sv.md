---
title: Aspose.3D for Java 21,2 Utgivning
type: docs
weight: 11
url: /sv/java/aspose-3d-for-java-21-2-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.2

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-825 |Lägg till USDZ import stöd.|Ny funktion|
|THREEDNET-824 |Lägg till texturstöd i USDZ|Uppgifter|
|THREEDNET-811 |Genomföra ett utvärderingsrelaterat undantag i API|Förbättring|
|THREEDNET-813 |Tekniska detaljer krävs för material och textur API begränsningar - API ger inte ett sätt att upptäcka texturer på material|Förbättring|
|THREEDNET-817 |Lägg till stöd för texturbyte[]i fallet av glb, gltf, obj|Förbättring|
|THREEDAPP-80 |Förbättra sidans lasthastighet för webben återgivning|Förbättring|
|THREEDNET-814 |Triangelindexen är inte korrekt|Felrättning|
|THREEDNET-809 |FBX Spara undantag: Typ som inte stöds|Felrättning|
|THREEDNET-810 |Filesize blir större när man återanvänder samma textur.|Felrättning|
|THREEDNET-816 |Felaktig maska vid lastning OBJ|Felrättning|
|THREEDNET-807 |Det finns ingen textur i den exporterade FBX|Felrättning|
|THREEDNET-815 |Material med shader modell = Okänt kommer inte att visas.|Felrättning|
|THREEDNET-823 |Flera maskor som fästs vid samma nod är inte rendering.|Felrättning|
|THREEDNET-647 |Lägg till skalkontroll användargränssnitt i webben renderare.|Uppgifter|
|THREEDNET-646 |Lägg till rotationskontroll användargränssnitt i webben renderare.|Uppgifter|



## API ändringar ##

### Tillagd klass `com.aspose.threed.TextureSlot`

Detta exponerade de interna textur slots i material, för att få tillgång till alla tillgängliga textur slots från ett material, använd för varje uttalande:

{{< highlight "java" >}}
        var mat = new PbrMaterial();
        for(var textureSlot : mat) {
            System.out.println(textureSlot.getSlotName());
            System.out.println(textureSlot.getTexture());
        }
{{< /highlight >}}

### Tillagd klass `com.aspose.threed.TrialException`

Från 21.2 när den olicensierade användningen nådde licensbegränsningen, En TrialException kommer att kastas för att meddela licensbegränsningen, och hur du ansöker om en tillfällig licens.

Du kan helt enkelt ignorera detta genom surround prov/fångsblock på Spara/öppna operationen, eller stänga av detta undantag genom att:

{{< highlight "java" >}}
        TrialException.setSuppressTrialException(true);
{{< /highlight >}}

Stäng av meddelandet kommer inte att lyfta begränsningarna (Liksom extra noder ignoreras av exportör/importör).

För att få alla funktioner, vänligen begär en tillfällig licens eller köp en fullständig funktionslicens.

### Lagt metoder till `com.aspose.threed.TriMesh`


{{< highlight "java" >}}
    /**
     * Read the vector4 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector4/FVector4 data type
     */
    public Vector4 readVector4(int idx, VertexField field);
  
    /**
     * Read the vector4 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector4/FVector4 data type
     */
    public FVector4 readFVector4(int idx, VertexField field);
  
      /**
     * Read the vector3 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector3/FVector3 data type
     */
    public Vector3 readVector3(int idx, VertexField field);
    
    /**
     * Read the vector3 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector3/FVector3 data type
     */
    public FVector3 readFVector3(int idx, VertexField field);

  
    /**
     * Read the vector2 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector2/FVector2 data type
     */
    public Vector2 readVector2(int idx, VertexField field);
    
    /**
     * Read the vector2 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector2/FVector2 data type
     */
    public FVector2 readFVector2(int idx, VertexField field);

  
    /**
     * Read the double field
     * @param idx The index of vertex to read
     * @param field The field with a float/double compatible data type
     */
    public double readDouble(int idx, VertexField field);
    
    /**
     * Read the float field
     * @param idx The index of vertex to read
     * @param field The field with a float/double compatible data type
     */
    public float readFloat(int idx, VertexField field);
{{< /highlight >}}


Dessa metoder tillåter dig att läsa vertex fält utan att tilldela extra minne, det traditionella sättet att komma åt vertex från `TriMesh` faktiskt genererar en hel del tillfälliga objekt, Dessa kan ge tillgång till snabbt och lågt minne avtryck.

{{< highlight "java" >}}
Scene s = ny Scene ("test.STL");
Var mesh = (Mesh)s.getRootNode().getChild(0).getEntity();

// Skapa en ny VertexDeclaration, så TriMesh vi skapade senare kommer att använda denna minnes layout.
Var vd = ny VertexDeclaration().
Var pos = vd. addField( VertexFieldDataType. F_VECTOR3, VertexFieldSemantic. BESTÄMMELSER
Var normal = vd. addField( VertexFieldDataType. F_VECTOR3, VertexFieldSemantic. NORMAL.
//Skapa en TriMesh instans från Mesh instans med manuellt angiven vertexdeklaration
Var m = TriMesh.frånMesh(vd, mesh).
För(int i = 0; i< m.getVerticesCount(); i++)
        {
            //access each field
            var v_pos = m.readFVector3(i, pos);
            var v_normal = m.readFVector3(i, normal);
            System.out.printf("(%s), (%s)\n", v_pos, v_normal);
        }
{{< /highlight >}}


### Lagt till nytt filformat i `com.aspose.threed.FileFormat`

{{< highlight "java" >}}
    /**
     * Compressed Universal Scene Description
     */
    public static final FileFormat USDZ;
{{< /highlight >}}

Aspose.3D 21.2 kan ladda USDZ format nu.


### Fixat inkonsekventa API:

Dessa gamla klasser flyttas till paket com. Förmodligen. Tre. och nya klasser införs för att ersätta dem:

|**Gammal klass** |**Ny klass** |
|:- |:- |
|Com.aspose. tre.A3DWaveOptions|Com.aspose. Threed.A3dwSaveOptionComment|
|Com.aspose. Threed.AMFSaveOptions|Com.aspose. Threed.AmfSaveOptionComment|
|Com.aspose. Threed.Discreet3DSLoadOptionsName|Com.aspose. Threed.Discreet3dsLoadOptioner|
|Com.aspose. Threed.Discreet3DSSaveOption|Com.aspose. Threed.Discreet3dsSaveOptioner|
|Com.aspose. Threed.FBXLoadOptionsComment|Com.aspose. Threed.FbxLoadOptionsComment|
|Com.aspose. Threed.FBXSaveOption|Com.aspose. Threed.FbxSaveOption|
|Com.aspose. Threed.GLTFLoadOptionsComment|Com.aspose. Threed.GltfLoadOptionsName|
|Com.aspose. Threed.GLTFSaveOptionComment|Com.aspose. Threed.GltfSaveOptioner|
|Com.aspose. Threed.HTML5SaveOptionComment|Com.aspose. Threed.Html5SparaOptionComment|
|Com.aspose. Threed.STLLoadOptions|Com.aspose. Threed.StlLoadOptionsComment|
|Com.aspose. Threed.STLSaveOptions|Com.aspose. Threed.StlSaveOptionComment|
|Com.aspose. Threed.U3DLoadOptionsName|Com.aspose. Threed. U3dLoadOptionsComment|


