---
title: Aspose.3D for Java Note di rilascio 21.7
type: docs
weight: 6
url: /it/java/aspose-3d-for-java-21-7-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.7.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-870 |Supporto per l'esportazione in formato USDZ.|Nuova funzione|
|THREEDNET-901 |Consentire all'utente di specificare una classe di fabbrica per FileSystem per migliorare il livello di sicurezza|Nuova funzionalità|
|THREEDNET-902 |Aggiungi GeomSubset nell'esportatore USDC per supportare più materiali|Miglioramento|
|THREEDNET-903 |GLTF Salvataggio dei nomi dei materiali di supporto|Miglioramento|
|THREEDNET-905 |USD file contenenti scheletro non sono supportati.|Correzione di bug|
|THREEDNET-904 |USD file contenenti normali come primvars non sono supportati.|Correzione di bug|
|THREEDNET-909 |USD allo GLTF utilizzato oltre la memoria 9G.|Correzione di bug|





## API modifiche ##



### Aggiunto USDZ come tipo di esportazione ###

Da 21.7 puoi esportare la scena in USDZ da:

{{< highlight "java" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.Save("test.usdz", FileFormat.USDZ);
{{< /highlight >}}


### Aggiunta classe com.aspose.threed.FileSystemFactory ###


{{< highlight "java" >}}
    /**
    * {@link com.aspose.threed.SaveOptions} and {@link com.aspose.threed.LoadOptions} will create a {@link com.aspose.threed.LocalFileSystem} for default.
    * This can be a security issue in server environment.
    * Use your own {@link com.aspose.threed.FileSystemFactory} to {@link com.aspose.threed.IOConfig#getFileSystemFactory} to improve server side security.
    */
    public interface FileSystemFactory
    {    
        FileSystem call();
        
    }
{{< /highlight >}}


### Aggiunta nuova proprietà FileSystemFactory a com.aspose.threed.IOConfig:


{{< highlight "java" >}}
    /**
     * Gets the factory class for FileSystem.
     * The default factory will create {@link com.aspose.threed.LocalFileSystem} which is not suitable for server environment.
     */
    public static FileSystemFactory getFileSystemFactory();
    
    /**
     * Sets the factory class for FileSystem.
     * The default factory will create {@link com.aspose.threed.LocalFileSystem} which is not suitable for server environment.
     * @param value New value
     */
    public static void setFileSystemFactory(FileSystemFactory value);

{{< /highlight >}}



Potrebbe essere pericoloso se l'utente ha creato un file 3D dannoso e caricato il contenuto sul server, il nuovo FileSystemFactory consente di specificare la propria implementazione di FileSystem per sostituire il LocalFileSystem originale che può leggere i dati sensibili durante l'esportazione di un file 3D.







### Aggiunta nuova proprietà a com.aspose.threed.FileFormat:

{{< highlight "java" >}}
    /**
     * Gets whether Aspose.3D supports export scene to current file format.
     */
    public boolean getCanExport();
    
    /**
     * Gets whether Aspose.3D supports import scene from current file format.
     */
    public boolean getCanImport();

{{< /highlight >}}

È possibile verificare se un formato di file supporta l'importazione o l'esportazione tramite queste proprietà.