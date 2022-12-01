---
title: Aspose.3D for .NET 21,2 Utgivning
type: docs
weight: 11
url: /sv/net/aspose-3d-for-net-21-2-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 21.2

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



### Lagt till klass Aspose.ThreeD.Shading.TextureSlott

Detta exponerade de interna textur slots i material, för att få tillgång till alla tillgängliga textur slots från ett material, använd för varje uttalande:

{{< highlight "csharp" >}}
var mat = new PbrMaterial();
foreach(var textureSlot in mat)
{
    Console.WriteLine(textureSlot.SlotName);
    Console.WriteLine(textureSlot.Texture);
}
{{< /highlight >}}


### Tillagd klass Aspose.ThreeD.

Från 21.2 när den olicensierade användningen nådde licensbegränsningen, En TrialException kommer att kastas för att meddela licensbegränsningen, och hur du ansöker om en tillfällig licens.

Du kan helt enkelt ignorera detta genom surround prov/fångsblock på Spara/öppna operationen, eller stänga av detta undantag genom att:

{{< highlight "csharp" >}}
TrialException.SuppressTrialException = true;
{{< /highlight >}}

Stäng av meddelandet kommer inte att lyfta begränsningarna (Liksom extra noder ignoreras av exportör/importör).

För att få alla funktioner, vänligen begär en tillfällig licens eller köp en fullständig funktionslicens.

### Tillagda metoder till Aspose.ThreeD.Enheter.TriMesh


{{< highlight "csharp" >}}
public Aspose.ThreeD.Utilities.Vector4 ReadVector4(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.FVector4 ReadFVector4(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.Vector3 ReadVector3(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.FVector3 ReadFVector3(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.Vector2 ReadVector2(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.FVector2 ReadFVector2(int idx, Aspose.ThreeD.Utilities.VertexField field);
public double ReadDouble(int idx, Aspose.ThreeD.Utilities.VertexField field);
public float ReadFloat(int idx, Aspose.ThreeD.Utilities.VertexField field);
{{< /highlight >}}

Dessa metoder tillåter dig att läsa vertex fält utan att tilldela extra minne, Det traditionella sättet att komma åt vertex från TriMesh faktiskt genererar en hel del tillfälliga objekt, Dessa kan ge tillgång till snabbt och lågt minne avtryck.

{{< highlight "csharp" >}}
Scene s = ny Scene(@"test.STL").
Var mesh = (Mesh)s.RootNode.ChildNodes[0].Entity;

// Skapa en ny VertexDeclaration, så TriMesh vi skapade senare kommer att använda denna minnes layout.
Var vd = ny VertexDeclaration().
Var pos = vd. Tilläggsfält( VertexFieldDataType. FVector3, VertexFieldSemantic. Position.
Var normal = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Normal;
Var uv = vd.AddField(VertexFieldDataType.FVector2, VertexFieldSemantic.UV.
//Skapa en TriMesh instans från Mesh instans med manuellt angiven vertexdeklaration
Var m = TriMesh.FromMesh(vd, mesh).
För(int i = 0; i< m.VerticesCount; i++)
{
    //access each field
    var v_pos = m.ReadFVector3(i, pos);
    var v_normal = m.ReadFVector3(i, normal);
    var v_uv = m.ReadFVector3(i, uv);
    Console.WriteLine($"({v_pos}), ({v_uv}), ({v_normal})");
}
{{< /highlight >}}

### Lagt till nytt filformat i Aspose.ThreeD.FileFormatt

{{< highlight "csharp" >}}
/// <summary>
/// Compressed Universal Scene Description
/// </summary>
public static readonly FileFormat USDZ;
{{< /highlight >}}

Aspose.3D 21.2 kan ladda USDZ format nu.


### Fixat inkonsekventa API:

Dessa gamla klasser kommer att hållas en tid, och nya klasser introduceras för att ersätta dem:

|**Gammal klass** |**Ny klass** |
|:- |:- |
|Aspose.ThreeD. Format.A3DWSaveOptioner|Aspose.ThreeD. Format.A3dwSaveOptioner|
|Aspose.ThreeD.Formats.AMFSparaOptioner|Aspose.ThreeD.Formats.AmfSparaOptioner|
|Aspose.ThreeD. Format.Discreet3DSLoadOptionsName|Aspose.ThreeD.Formats.Discreet3dsLoadOptioner|
|Aspose.ThreeD.Formats.Discreet3DSSaveOptioner|Aspose.ThreeD. Format.Discreet3dssparaOptioner|
|Aspose.ThreeD. Format.FBXLoadOptionsName|Aspose.ThreeD.Formats.FbxLoadOptioner|
|Aspose.ThreeD. Format.FBXSaveOptioner|Aspose.ThreeD. Format.FbxSaveOptioner|
|Aspose.ThreeD. Format.GLTFLoadOptionsGenericName|Aspose.ThreeD.Formats.GltfLoadOptioner|
|Aspose.ThreeD.Formats.GLTFSparaOptioner|Aspose.ThreeD. Format.GltfSparaOptioner|
|Aspose.ThreeD. Format.HTML5SparaOptioner|Aspose.ThreeD. Format.Html5SparaOptioner|
|Aspose.ThreeD.Format.STLLoadOptioner|Aspose.ThreeD.Formats.StlLoadOptioner|
|Aspose.ThreeD.Formats.STLSaveOptioner|Aspose.ThreeD. Format.StlSaveOptioner|
|Aspose.ThreeD. Format.U3DLoadOptions.|Aspose.ThreeD. Format.U3dLoadOptions.|
