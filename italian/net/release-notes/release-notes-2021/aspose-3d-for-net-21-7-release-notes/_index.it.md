---
title: Aspose.3D for .NET Note di rilascio 21.7
type: docs
weight: 6
url: /it/net/aspose-3d-for-net-21-7-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 21.7.

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

{{< highlight "csharp" >}}
    Scene scene = new Scene();
    //...prepare your scene
    scene.Save("test.usdz", FileFormat.USDZ);
{{< /highlight >}}


### Classe aggiunta Aspose.ThreeD.Formats.FileSystemFactory ###


{{< highlight "csharp" >}}
    /// <summary>
    /// <see cref="SaveOptions"/> and <see cref="LoadOptions"/> will create a <see cref="LocalFileSystem"/> for default.
    /// This can be a security issue in server environment.
    /// Use your own <see cref="FileSystemFactory"/> to <see cref="IOConfig.FileSystemFactory"/> to improve server side security.
    /// </summary>
    /// <returns></returns>
    public delegate FileSystem FileSystemFactory();
{{< /highlight >}}


### Aggiunta la nuova proprietà FileSystemFactory allo Aspose.ThreeD.Formats.IOConfig:


{{< highlight "csharp" >}}
        /// <summary>
        /// Gets or sets the factory class for FileSystem.
        /// The default factory will create <see cref="LocalFileSystem"/> which is not suitable for server environment.
        /// </summary>
        public static FileSystemFactory FileSystemFactory { get; set; }
{{< /highlight >}}



Potrebbe essere pericoloso se l'utente ha creato un file 3D dannoso e caricato il contenuto sul server, il nuovo FileSystemFactory consente di specificare la propria implementazione di FileSystem per sostituire il LocalFileSystem originale che può leggere i dati sensibili durante l'esportazione di un file 3D.







### Aggiunta nuova proprietà allo Aspose.ThreeD.FileFormat:

{{< highlight "csharp" >}}
        /// <summary>
        /// Gets whether Aspose.3D supports export scene to current file format.
        /// </summary>
        public bool CanExport { get; set; }
        /// <summary>
        /// Gets whether Aspose.3D supports import scene from current file format.
        /// </summary>
        public bool CanImport { get; set; }
{{< /highlight >}}

È possibile verificare se un formato di file supporta l'importazione o l'esportazione tramite queste proprietà.