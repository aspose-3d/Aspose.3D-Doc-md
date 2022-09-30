---
title: Aspose.3D for .NET 21.6 Note di rilascio
type: docs
weight: 7
url: /it/net/aspose-3d-for-net-21-6-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 21.6.

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
    scene.Save("test.usd", FileFormat.USD);
{{< /highlight >}}

### Aggiunta nuova classe Aspose.ThreeD.Utilities.ZipArchiveFileSystem ###

È possibile per glb/fbx e altri formati di file che supportano l'incorporamento di texture per accedere alle risorse esterne tramite un file zip utilizzando un ZipArchiveFileSystem per SaveOptions.FileSystem.


### Aggiunta nuova proprietà alla classe Aspose.ThreeD.Formats.FbxSaveOptions ###

{{< highlight "csharp" >}}
    /// <summary>
    /// Gets or sets whether to embed the texture to the final output file.
    /// FBX Exporter will try to find the texture's raw data from <see cref="IOConfig.FileSystem"/>, and embed the file to final FBX file.
    /// Default value is false.
    /// </summary>
    public bool EmbedTextures{ get;set;}
{{< /highlight >}}


Codice del campione:

{{< highlight "java" >}}
    var scene = new Scene();
    var opt = new FbxSaveOptions(FileFormat.FBX7700ASCII);
    opt.EmbedTextures = true;
    var tex = new Texture();
    tex.FileName = "test.png";
    tex.SetProperty("RelativeFilename", "test.png");
    var mat = new PhongMaterial();
    mat.SetTexture(Material.MapDiffuse, tex);
    var planeNode = scene.RootNode.CreateChildNode(new Plane());
    planeNode.Material = mat;
    scene.Save("plane-with-texture.fbx", opt);

{{< /highlight >}}


### Classe obsoleta rimossa Aspose.ThreeD. Formati. A3DWSaveOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. AMFSaveOptions
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. Discreet3DSLoadOptions
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Rimossa la classe obsoleta Aspose.ThreeD. Formati. Discreet3DSSaveOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. FBXLoadOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. FBXSaveOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. GLTFLoadOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. GLTFSaveOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. HTML5SaveOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Rimossa la classe obsoleta Aspose.ThreeD. Formati. STLLoadOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. STLSaveOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.

### Classe obsoleta rimossa Aspose.ThreeD. Formati. U3DLoadOptions ###
Questa classe è stata contrassegnata come obsoleta mesi prima.
