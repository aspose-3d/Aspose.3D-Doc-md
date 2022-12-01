---
title: Aspose.3D for .NET 21.2 Note di rilascio
type: docs
weight: 11
url: /it/net/aspose-3d-for-net-21-2-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 21.2.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-825 |Aggiungi il supporto per l'importazione USDZ.|Nuova funzionalità|
|THREEDNET-824 |Aggiungi supporto texture nel USDZ|Attività|
|THREEDNET-811 |Implementare una versione di valutazione relativa all'eccezione nello API|Miglioramento|
|THREEDNET-813 |I dettagli tecnici sono richiesti su Material and Texture API limitazioni-API non fornisce un modo per scoprire le trame sui materiali|Miglioramento|
|THREEDNET-817 |Aggiungere il supporto per il byte di texture []in caso di glb, gltf, obj|Miglioramento|
|THREEDAPP-80 |Migliorare la velocità di caricamento della pagina del renderer web|Miglioramento|
|THREEDNET-814 |Gli indici del triangolo non sono corretti|Correzione di bug|
|THREEDNET-809 |FBX Salva eccezione: tipo di attributo non supportato|Correzione di bug|
|THREEDNET-810 |Il file sta diventando più grande durante il riutilizzo della stessa texture|Correzione di bug|
|THREEDNET-816 |Maglia errata durante il caricamento OBJ|Correzione di bug|
|THREEDNET-807 |Non c' è consistenza nello FBX esportato|Correzione di bug|
|THREEDNET-815 |Materiali con modello shader = Unknown non è riuscito a eseguire il rendering.|Correzione di bug|
|THREEDNET-823 |La mesh multipla collegata allo stesso nodo non è in rendering.|Correzione di bug|
|THREEDNET-647 |Aggiungere l'interfaccia utente di controllo di ridimensionamento nel renderer Web.|Attività|
|THREEDNET-646 |Aggiungere l'interfaccia utente di controllo della rotazione nel renderer Web.|Attività|


## API modifiche ##



### Classe aggiunta Aspose.ThreeD.Shading.TextureSlot

Questo ha esposto gli slot texture interni nei materiali, al fine di accedere a tutti gli slot texture disponibili da un materiale, utilizzare per ogni dichiarazione:

{{< highlight "csharp" >}}
var mat = new PbrMaterial();
foreach(var textureSlot in mat)
{
    Console.WriteLine(textureSlot.SlotName);
    Console.WriteLine(textureSlot.Texture);
}
{{< /highlight >}}


### Classe aggiunta Aspose.ThreeD.TrialException

A partire da 21.2, quando l'utilizzo senza licenza ha raggiunto la restrizione della licenza, verrà lanciata una TrialException per notificare la restrizione della licenza e come richiedere una licenza temporanea.

Puoi semplicemente ignorarlo surround try/catch block sull'operazione Salva/Apri o disattivare questa eccezione:

{{< highlight "csharp" >}}
TrialException.SuppressTrialException = true;
{{< /highlight >}}

Disattivare questo messaggio non eliminerà le restrizioni (come i nodi extra vengono ignorati dall'esportatore/importatore).

Per ottenere tutte le funzionalità complete, richiedi una licenza temporanea o acquista una licenza completa.

### Metodi aggiunti a Aspose.ThreeD.Entities.TriMesh


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

Questi metodi consentono di leggere il campo del vertice senza allocare memoria extra, il modo tradizionale di accedere al vertice da TriMesh genera effettivamente molti oggetti temporanei, questi possono fornire un accesso rapido e a bassa memoria.

{{< highlight "csharp" >}}
Scene s = nuova scena (@ "test.STL");
Var mesh = (Mesh)s. NootNode. ChildNodes[0]. Entità;

// Crea una nuova VertexDeclaration, quindi il TriMesh che abbiamo costruito in seguito utilizzerà questo layout di memoria.
Var vd = new VertexDeclaration();
Var pos = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);
Var normal = vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Normal);
Var uv = vd.AddField(VertexFieldDataType.FVector2, VertexFieldSemantic.UV);
// Crea un'istanza TriMesh dall'istanza Mesh con la dichiarazione del vertice specificata manualmente
Var m = TriMesh.FromMesh(vd, mesh);
Per (int i = 0; i< m.VerticesCount; i++)
{
    //access each field
    var v_pos = m.ReadFVector3(i, pos);
    var v_normal = m.ReadFVector3(i, normal);
    var v_uv = m.ReadFVector3(i, uv);
    Console.WriteLine($"({v_pos}), ({v_uv}), ({v_normal})");
}
{{< /highlight >}}

### Aggiunto nuovo formato di file in Aspose.ThreeD.FileFormat

{{< highlight "csharp" >}}
/// <summary>
/// Compressed Universal Scene Description
/// </summary>
public static readonly FileFormat USDZ;
{{< /highlight >}}

Aspose.3D 21.2 può caricare ora il formato USDZ.


### Risolto le API incoerenti:

Queste vecchie classi saranno mantenute per un po 'e vengono introdotte nuove classi per sostituirle:

|**Vecchia classe** |**Nuova classe** |
|:- |:- |
|Aspose.ThreeD. Formati. A3DWSaveOptions|Aspose.ThreeD. Formati. A3dwSaveOptions|
|Aspose.ThreeD. Formati. AMFSaveOptions|Aspose.ThreeD. Formati. AmfSaveOptions|
|Aspose.ThreeD. Formati. Discreet3DSLoadOptions|Aspose.ThreeD. Formati. Discreet3dsLoadOptions|
|Aspose.ThreeD. Formati. Discreet3DSSaveOptions|Aspose.ThreeD. Formati. Discreet3dsSaveOptions|
|Aspose.ThreeD. Formati. FBXLoadOptions|Aspose.ThreeD. Formati. FbxLoadOptions|
|Aspose.ThreeD. Formati. FBXSaveOptions|Aspose.ThreeD. Formati. FbxSaveOptions|
|Aspose.ThreeD. Formati. GLTFLoadOptions|Aspose.ThreeD. Formati. GltfLoadOptions|
|Aspose.ThreeD. Formati. GLTFSaveOptions|Aspose.ThreeD. Formati. GltfSaveOptions|
|Aspose.ThreeD. Formati. HTML5SaveOptions|Aspose.ThreeD. Formati. Html5SaveOptions|
|Aspose.ThreeD. Formati. STLLoadOptions|Aspose.ThreeD. Formati. StlLoadOptions|
|Aspose.ThreeD. Formati. STLSaveOptions|Aspose.ThreeD. Formati. StlSaveOptions|
|Aspose.ThreeD. Formati. U3DLoadOptions|Aspose.ThreeD. Formati. U3dLoadOptions|
