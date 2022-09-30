---
title: Aspose.3D for .NET 20.10 Note di rilascio
type: docs
weight: 7
url: /it/net/aspose-3d-for-net-20-10-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.10.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-737 |Aggiungi supporto primitivo in A3DW export/import.|
|THREEDNET-732 |Aspose.3D ha un errore di trama durante la generazione dello GLTF, ma non ci sono problemi a salvarlo come FBX|
|THREEDNET-738 |Aggiungi il supporto della tabella dei colori nel file RVM.|
|THREEDNET-739 |Supporto per 7.7/Binary/Autodesk FBX|

## API modifiche ##

### Aggiunti nuovi formati di file alla classe Aspose.ThreeD.FileFormat:

{{< highlight "java" >}}

    public static readonly Aspose.ThreeD.FileFormat FBX7600ASCII;
    public static readonly Aspose.ThreeD.FileFormat FBX7600Binary;
    public static readonly Aspose.ThreeD.FileFormat FBX7700ASCII;
    public static readonly Aspose.ThreeD.FileFormat FBX7700Binary;

{{< /highlight >}}

Ora è possibile esportare la scena in FBX 7.6/7.7 in modalità ASCII/Binary.

Codice del campione:

{{< highlight "java" >}}

    Scene scene = new Scene(new Pyramid());
    scene.Save("fbx7.7.fbx", FileFormat.FBX7700ASCII);

{{< /highlight >}}


### Aggiunta nuova classe Aspose.ThreeD. Formati. A3DWSaveOptions

{{< highlight "java" >}}

    /// <summary>
    /// Save options for A3DW format.
    /// </summary>
    public class A3DWSaveOptions : SaveOptions
    {
        /// <summary>
        /// Export meta data associated with Scene/Node to client
        /// Default value is true
        /// </summary>
        public bool ExportMetaData { get; set; }

        /// <summary>
        /// If this property is non-null, only the properties of Scene/Node that start with this prefix will be exported, and the prefix will be removed.
        /// </summary>
        public string MetaDataPrefix { get; set; }
    }

{{< /highlight >}}

Il nuovo A3DWSaveOptions consente di esportare le informazioni e le proprietà delle risorse in un file A3DW.

Viene utilizzato con il nostro nuovo renderer Web in arrivo.

{{< highlight "java" >}}

    Scene scene = new Scene();
    scene.RootNode.CreateChildNode(new Pyramid()).SetProperty("rvm:No", "347923");
    scene.Save("test.a3dw", new A3DWSaveOptions() { MetaDataPrefix = "rvm:" });

{{< /highlight >}}
