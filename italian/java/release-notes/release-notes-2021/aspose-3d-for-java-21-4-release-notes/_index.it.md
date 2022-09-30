---
title: Aspose.3D for Java 21.4 Note di rilascio
type: docs
weight: 9
url: /it/java/aspose-3d-for-java-21-4-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.4.

{{% /alert %}}
## **Miglioramenti e modifiche**
|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-864 |Implementare la proprietà FileStream per Texture Class per caricare l'immagine da un flusso|Miglioramento|
|THREEDNET-867 |File obj di grandi dimensioni prendere un sacco di tempo per caricare|Miglioramento|
|THREEDNET-865 |Aggiungere il materiale compatibile con Autodesk Navisworks per il formato RVM|Miglioramento|
|THREEDNET-874 |Aggiungi il supporto dell'ultimo formato RVM.|Miglioramento|
|THREEDAPP-94 |Miglioramento delle prestazioni di caricamento del renderer Web|Miglioramento|
|THREEDNET-851 |Consentire l'utilizzo dell'implementazione esterna dell'encoder Draco.|Miglioramento|
|THREEDNET-876 |Migliorare le prestazioni builtin Draco encoder/decoder.|Miglioramento|
|THREEDNET-862 |Il file glb convertito non può essere aperto da strumenti di terze parti.|Correzione di bug|
|THREEDNET-863 |La conversione da USDZ a STL fallisce|Correzione di bug|
|THREEDNET-866 |FBX a gltf/glb ExportExportException: Tipo di oggetto Aspose.ThreeD.Utilities. Vector3non è supportato|Correzione di bug|
|THREEDNET-873 |Collada esportati da Frosty Suite non possono essere importati.|Correzione di bug|
|THREEDNET-872 |Collada esportato dallo strumento frullatore/lego non può essere importato.|Correzione di bug|
|THREEDNET-871 |Alcuni file Zipped 3D non possono essere aperti dallo Aspose.3D|Correzione di bug|
|THREEDNET-869 |Alcuni file STL non sono riconosciuti|Correzione di bug|
|THREEDAPP-114 |I file binari STL senza un'intestazione binaria esplicita non possono essere aperti.|Correzione di bug|


## API modifiche ##


Questa versione è principalmente una versione per la correzione di bug, ha risolto molti bug e migliorato molti problemi di compatibilità e prestazioni per FBX, Collada, STL, obj, drc, gltf, glb.



Solo alcune modifiche minori API.

### Aggiunta nuova proprietà in classe `com.aspose.threed.GltfSaveOptions`:

{{< highlight "java" >}}

    /**
     * Use external draco encoder to accelerate the draco compression speed.
     */
    public String getExternalDracoEncoder();
    
    /**
     * Use external draco encoder to accelerate the draco compression speed.
     * @param value New value
     */
    public void setExternalDracoEncoder(String value);


{{< /highlight >}}


Aspose.3D per java 21.4 ha un miglioramento delle prestazioni doppio per Draco rispetto alle vecchie versioni, ma l'implementazione ufficiale dello Google scritta nello C++ è ancora più veloce, quindi consentiamo all'utente di utilizzare l'encoder esterno Draco per prestazioni migliori.


Codice di esempio per utilizzare encoder ufficiale esterno per accelerare la generazione compressa GLB:

{{< highlight "java" >}}

        var mesh = new Sphere();
        var scene = new Scene(mesh);
        var opt = new GltfSaveOptions(FileFormat.GLTF2__BINARY);
        opt.setExternalDracoEncoder("D:\\Github\\draco\\sln\\Release\\draco_encoder.exe");
        opt.setDracoCompression(true);
        scene.save("test.glb", opt);

{{< /highlight >}}


{{% alert color="primary" %}} 
NOTA: questa proprietà verrà contrassegnata come obsoleta una volta migliorate le prestazioni di codifica/decodifica draco a livello di implementazione ufficiale.
{{% /alert %}}

