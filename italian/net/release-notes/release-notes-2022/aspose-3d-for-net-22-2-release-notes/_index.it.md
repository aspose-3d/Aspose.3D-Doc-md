---
title: Aspose.3D for .NET Note di rilascio 22.2
type: docs
weight: 11
url: /it/net/aspose-3d-for-net-22-2-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 22.2.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1054 |Consenti incorporare le trame nei file U3D e PDF|Nuova funzionalità|
|THREEDNET-1058 |I primitivi non possono essere vincolati al materiale nell'esportatore/importatore USD|Correzione di bug|
|THREEDNET-1051 |Consenti l'accesso extra ed estensioni nel file GLTF|Miglioramento|
|THREEDNET-1048 |Consenti di codificare i meta dati della scena e del nodo a usd|Nuova funzionalità|
|THREEDNET-1049 |Consenti decodifica i metadati della scena e del nodo da usd|Nuova funzionalità|

## API modifiche ##


### Membri aggiunti alla classe `Aspose.ThreeD.AssetInfo`:

{{< highlight "csharp" >}}
        public string Copyright{ get;set;}
{{< /highlight >}}

Ottiene il copyright del file, questo valore può essere nullo o definito nel file 3D.
Solo USDC/USDZ supporta questa proprietà ora.

NOTA: Le modifiche in questa proprietà non cambieranno la sezione del copyright del file di output 3D.


### Membri aggiunti alla classe `Aspose.ThreeD.Formats.UsdSaveOptions`:

{{< highlight "csharp" >}}
        public bool ExportMetaData{ get;set;}
{{< /highlight >}}

Ottiene o imposta se esportare le informazioni sulle risorse della scena e le proprietà del nodo nel file USDC/USDZ di output.



### Membri aggiunti alla classe `Aspose.ThreeD.Formats.PdfSaveOptions`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Embed the external textures into the PDF file, default value is false.
        /// </summary>
        public bool EmbedTextures{ get;set;}
{{< /highlight >}}

Imposta questo su true per generare file 3D PDF con file texture incorporati.

Esempio di codice:

{{< highlight "csharp" >}}
        var scene = new Scene();
        scene.Open($"test.obj");
        var opt = new PdfSaveOptions();
        //embed the external textures in the output PDF file.
        opt.EmbedTextures = true;
        //Look up external textures in the  common/textures directory
        opt.LookupPaths.Add("common/textures");
        scene.Save("test.pdf", opt);
{{< /highlight >}}


### Membri aggiunti alla classe `Aspose.ThreeD.Formats.U3dSaveOptions`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Embed the external textures into the U3D file, default value is false.
        /// </summary>
        public bool EmbedTextures{ get;set;}
{{< /highlight >}}

Imposta questo su true per generare file 3D U3D con file texture incorporati.

Esempio di codice:

{{< highlight "csharp" >}}
        var scene = new Scene();
        scene.Open($"test.obj");
        var opt = new U3dSaveOptions();
        //embed the external textures in the output PDF file.
        opt.EmbedTextures = true;
        //Look up external textures in the  common/textures directory
        opt.LookupPaths.Add("common/textures");
        scene.Save("test.u3d", opt);
{{< /highlight >}}



