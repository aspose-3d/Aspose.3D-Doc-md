---
title: Aspose.3D for Java Note di rilascio 22.2
type: docs
weight: 11
url: /it/java/aspose-3d-for-java-22-2-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 22.2.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEJava-1054|Consenti incorporare le trame nei file U3D e PDF|Nuova funzionalità|
|THREEJava-1058|I primitivi non possono essere vincolati al materiale nell'esportatore/importatore USD|Correzione di bug|
|THREEJava-1051|Consenti l'accesso extra ed estensioni nel file GLTF|Miglioramento|
|THREEJava-1048|Consenti di codificare i meta dati della scena e del nodo a usd|Nuova funzionalità|
|THREEJava-1049|Consenti decodifica i metadati della scena e del nodo da usd|Nuova funzionalità|

## API modifiche ##


### Aggiunti membri a class com.aspose.threed.AssetInfo:

{{< highlight "java" >}}
    /**
     * Gets the document's copyright
     */
    public String getCopyright();

{{< /highlight >}}

Ottiene il copyright del file, questo valore può essere nullo o definito nel file 3D.
Solo USDC/USDZ supporta questa proprietà ora.

NOTA: Le modifiche in questa proprietà non cambieranno la sezione del copyright del file di output 3D.


### Membri aggiunti alla classe `com.aspose.threed.UsdSaveOptions`:

{{< highlight "csharp" >}}
    /**
     * Export meta data associated with Scene/Node to client
     * Default value is true
     */
    public boolean getExportMetaData();
    
    /**
     * Export meta data associated with Scene/Node to client
     * Default value is true
     * @param value New value
     */
    public void setExportMetaData(boolean value);

{{< /highlight >}}

Ottiene o imposta se esportare le informazioni sulle risorse della scena e le proprietà del nodo nel file USDC/USDZ di output.



### Membri aggiunti alla classe `com.aspose.threed.PdfSaveOptions`:

{{< highlight "java" >}}
    /**
     * Embed the external textures into the PDF file, default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Embed the external textures into the PDF file, default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);
{{< /highlight >}}

Imposta questo su true per generare file 3D PDF con file texture incorporati.

Esempio di codice:

{{< highlight "java" >}}
        var scene = new Scene();
        scene.open("test.obj");
        var opt = new PdfSaveOptions();
        //embed the external textures in the output PDF file.
        opt.setEmbedTextures(true);
        //Look up external textures in the  common/textures directory
        opt.getLookupPaths().add("common/textures");
        scene.save("test.pdf", opt);
{{< /highlight >}}


### Membri aggiunti alla classe `com.aspose.threed.U3dSaveOptions`:

{{< highlight "java" >}}
    /**
     * Embed the external textures into the U3D file, default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Embed the external textures into the U3D file, default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);

{{< /highlight >}}

Imposta questo su true per generare file 3D U3D con file texture incorporati.

Esempio di codice:

{{< highlight "java" >}}
        var scene = new Scene();
        scene.open("test.obj");
        var opt = new U3dSaveOptions();
        //embed the external textures in the output PDF file.
        opt.setEmbedTextures(true);
        //Look up external textures in the  common/textures directory
        opt.getLookupPaths().add("common/textures");
        scene.save("test.u3d", opt);
{{< /highlight >}}



