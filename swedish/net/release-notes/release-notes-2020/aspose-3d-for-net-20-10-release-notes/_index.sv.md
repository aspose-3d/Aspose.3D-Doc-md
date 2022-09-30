---
title: Aspose.3D for .NET 20,10 Utgivning
type: docs
weight: 7
url: /sv/net/aspose-3d-for-net-20-10-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 20.10.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-737 |Lägg till primitivt stöd i A3DW export/import.|
|THREEDNET-732 |Aspose.3D har ett texturfel vid generering GLTF, men det finns inga problem med att spara det som FBX|
|THREEDNET-738 |Lägg till färgtabellstöd i RVM fil.|
|THREEDNET-739 |Stöd till 7.7/Binary/Autodesk FBX|

## API ändringar ##

### Lagt till nya filformat i klass Aspose.ThreeD.FileFormat:

{{< highlight "java" >}}

    public static readonly Aspose.ThreeD.FileFormat FBX7600ASCII;
    public static readonly Aspose.ThreeD.FileFormat FBX7600Binary;
    public static readonly Aspose.ThreeD.FileFormat FBX7700ASCII;
    public static readonly Aspose.ThreeD.FileFormat FBX7700Binary;

{{< /highlight >}}

Nu kan du exportera scenen till FBX 7.6/7.7 i ASCII/Binläge.

Provkod:

{{< highlight "java" >}}

    Scene scene = new Scene(new Pyramid());
    scene.Save("fbx7.7.fbx", FileFormat.FBX7700ASCII);

{{< /highlight >}}


### Lagt till ny klass Aspose.ThreeD.Formats.A3DWSaveOptions.

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

Den nya A3DWSaveOptions kan du exportera tillgång info och egenskaper till A3DW fil.

Detta används med vår nya inkommande webben renderare.

{{< highlight "java" >}}

    Scene scene = new Scene();
    scene.RootNode.CreateChildNode(new Pyramid()).SetProperty("rvm:No", "347923");
    scene.Save("test.a3dw", new A3DWSaveOptions() { MetaDataPrefix = "rvm:" });

{{< /highlight >}}
