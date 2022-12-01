---
title: Aspose.3D for Java 21.2 Note di rilascio
type: docs
weight: 11
url: /it/java/aspose-3d-for-java-21-2-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.2.

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

### Classe aggiunta `com.aspose.threed.TextureSlot`

Questo ha esposto gli slot texture interni nei materiali, al fine di accedere a tutti gli slot texture disponibili da un materiale, utilizzare per ogni dichiarazione:

{{< highlight "java" >}}
        var mat = new PbrMaterial();
        for(var textureSlot : mat) {
            System.out.println(textureSlot.getSlotName());
            System.out.println(textureSlot.getTexture());
        }
{{< /highlight >}}

### Classe aggiunta `com.aspose.threed.TrialException`

A partire da 21.2, quando l'utilizzo senza licenza ha raggiunto la restrizione della licenza, verrà lanciata una TrialException per notificare la restrizione della licenza e come richiedere una licenza temporanea.

Puoi semplicemente ignorarlo surround try/catch block sull'operazione Salva/Apri o disattivare questa eccezione:

{{< highlight "java" >}}
        TrialException.setSuppressTrialException(true);
{{< /highlight >}}

Disattivare questo messaggio non eliminerà le restrizioni (come i nodi extra vengono ignorati dall'esportatore/importatore).

Per ottenere tutte le funzionalità complete, richiedi una licenza temporanea o acquista una licenza completa.

### Metodi aggiunti allo `com.aspose.threed.TriMesh`


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


Questi metodi consentono di leggere il campo del vertice senza allocare memoria extra, il modo tradizionale di accedere al vertice dallo `TriMesh` genera effettivamente molti oggetti temporanei, questi possono fornire un accesso rapido e a bassa memoria.

{{< highlight "java" >}}
Scena s = nuova scena ("test.STL");
Var mesh = (Mesh)s.getRootNode().getChild(0).getEntity();

// Crea una nuova VertexDeclaration, quindi il TriMesh che abbiamo costruito in seguito utilizzerà questo layout di memoria.
Var vd = new VertexDeclaration();
Var pos = vd.addField(VertexFieldDataType.F _ VECTOR3, VertexFieldSemantic.POSITION);
Var normal = vd.addField(VertexFieldDataType.F _ VECTOR3, VertexFieldSemantic.NORMAL);
// Crea un'istanza TriMesh dall'istanza Mesh con la dichiarazione del vertice specificata manualmente
Var m = TriMesh.fromMesh(vd, mesh);
Per (int i = 0; i< m.getVerticesCount(); i++)
        {
            //access each field
            var v_pos = m.readFVector3(i, pos);
            var v_normal = m.readFVector3(i, normal);
            System.out.printf("(%s), (%s)\n", v_pos, v_normal);
        }
{{< /highlight >}}


### Aggiunto nuovo formato di file nel `com.aspose.threed.FileFormat`

{{< highlight "java" >}}
    /**
     * Compressed Universal Scene Description
     */
    public static final FileFormat USDZ;
{{< /highlight >}}

Aspose.3D 21.2 può caricare ora il formato USDZ.


### Risolto le API incoerenti:

Queste vecchie classi vengono spostate in package com.aspose.threed.de precated e vengono introdotte nuove classi per sostituirle:

|**Vecchia classe** |**Nuova classe** |
|:- |:- |
|Com. aspose.threed.A3DWSaveOptions|Com. aspose.threed.A3dwSaveOptions|
|Com. aspose.threed.AMFSaveOptions|Com. aspose.threed.AmfSaveOptions|
|Com. aspose.threed.Discreet3DSLoadOptions|Com. aspose.threed.Discreet3dsLoadOptions|
|Com. aspose.threed.Discreet3DSSaveOptions|Com. aspose.threed.Discreet3dsSaveOptions|
|Com. aspose.threed.FBXLoadOptions|Com. aspose.threed.FbxLoadOptions|
|Com. aspose.threed.FBXSaveOptions|Com. aspose.threed.FbxSaveOptions|
|Com. aspose.threed.GLTFLoadOptions|Com. aspose.threed.GltfLoadOptions|
|Com. aspose.threed.GLTFSaveOptions|Com. aspose.threed.GltfSaveOptions|
|Com. aspose.threed.HTML5SaveOptions|Com. aspose.threed.Html5SaveOptions|
|Com. aspose.threed.STLLoadOptions|Com. aspose.threed.StlLoadOptions|
|Com. aspose.threed.STLSaveOptions|Com. aspose.threed.StlSaveOptions|
|Com. aspose.threed.U3DLoadOptions|Com. aspose.threed.U3dLoadOptions|


