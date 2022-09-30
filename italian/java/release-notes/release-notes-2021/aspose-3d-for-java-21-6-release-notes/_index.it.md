---
title: Aspose.3D for Java 21.6 Note di rilascio
type: docs
weight: 7
url: /it/java/aspose-3d-for-java-21-6-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.6.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-870 |Aggiungi il supporto per l'esportazione USDC.|Nuova funzione|
|THREEDNET-891 |Esporre il file system dell'archivio zip|Nuova funzione|
|THREEDNET-892 |Consentire all'esportatore FBX di incorporare le trame durante l'esportazione.|Nuova funzionalità|
|THREEDNET-895 |Risolto alcuni caratteri nel nome del nodo, il file GLB generato non è riuscito a superare la convalida|Correzione di bug|
|THREEDNET-896 |La scena vuota fissa non può essere esportata in un file glb valido|Correzione di bug|
|THREEDNET-890 |Aggiungi esportazione materiale/texture in USDC|Miglioramento|
|THREEDNET-899 |Esporre la proprietà di RelativeFilename per la texture FBX|Miglioramento|




## API modifiche ##


### Aggiunto USD come tipo di esportazione ###

A partire da 21,6 è possibile esportare la scena in un file USD tramite:

{{< highlight "csharp" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.save("test.usd", FileFormat.USD);
{{< /highlight >}}

### Aggiunta nuova classe com.aspose.threed.ZipArchiveFileSystem ###

È possibile per glb/fbx e altri formati di file che supportano l'incorporamento di texture per accedere alle risorse esterne tramite un file zip utilizzando un ZipArchiveFileSystem per SaveOptions.FileSystem.


### Aggiunta nuova proprietà a class com.aspose.threed.FbxSaveOptions ###

{{< highlight "csharp" >}}
    /**
     * Gets whether to embed the texture to the final output file.
     * FBX Exporter will try to find the texture's raw data from {@link com.aspose.threed.IOConfig#getFileSystem}, and embed the file to final FBX file.
     * Default value is false.
     */
    public boolean getEmbedTextures();
    
    /**
     * Sets whether to embed the texture to the final output file.
     * FBX Exporter will try to find the texture's raw data from {@link com.aspose.threed.IOConfig#getFileSystem}, and embed the file to final FBX file.
     * Default value is false.
     * @param value New value
     */
    public void setEmbedTextures(boolean value);
{{< /highlight >}}


Codice del campione:

{{< highlight "java" >}}
    var scene = new Scene();
    var opt = new FbxSaveOptions(FileFormat.FBX7700ASCII);
    opt.setEmbedTextures(true);
    var tex = new Texture();
    tex.setFileName("test.png");
    var mat = new PhongMaterial();
    mat.setTexture(Material.MAP_DIFFUSE, tex);
    var planeNode = scene.getRootNode().createChildNode(new Plane());
    planeNode.setMaterial(mat);
    scene.save("plane-with-texture.fbx", opt);
{{< /highlight >}}

