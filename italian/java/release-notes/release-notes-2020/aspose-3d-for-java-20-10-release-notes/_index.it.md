---
title: Aspose.3D for Java 20.10 Note di rilascio
type: docs
weight: 7
url: /it/java/aspose-3d-for-java-20-10-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 20.10.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-737 |Aggiungi supporto primitivo in A3DW export/import.|
|THREEDNET-732 |Aspose.3D ha un errore di trama durante la generazione dello GLTF, ma non ci sono problemi a salvarlo come FBX|
|THREEDNET-738 |Aggiungi il supporto della tabella dei colori nel file RVM.|
|THREEDNET-739 |Supporto per 7.7/Binary/Autodesk FBX|


## API modifiche ##

### Aggiunti nuovi formati di file a class com.aspose.threed.FileFormat:

{{< highlight "java" >}}
    /**
     * ASCII FBX file format, with 7.6.0 version
     */
    public static final FileFormat FBX7600ASCII;
    /**
     * Binary FBX file format, with 7.6.0 version
     */
    public static final FileFormat FBX7600_BINARY;
    /**
     * ASCII FBX file format, with 7.7.0 version
     */
    public static final FileFormat FBX7700ASCII;
    /**
     * Binary FBX file format, with 7.7.0 version
     */
    public static final FileFormat FBX7700_BINARY;

{{< /highlight >}}

Ora è possibile esportare la scena in FBX 7.6/7.7 in modalità ASCII/Binary.

Codice del campione:

{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Pyramid());
    scene.save("fbx7.7.fbx", FileFormat.FBX7700_BINARY);

{{< /highlight >}}


### Aggiunta nuova classe com.aspose.threed.A3DWSaveOptions

{{< highlight "java" >}}


/**
 * Save options for A3DW format.
 */
public class A3DWSaveOptions extends SaveOptions
{    
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

    /**
     * If this property is non-null, only the properties of Scene/Node that start with this prefix will be exported, and the prefix will be removed.
     */
    public String getMetaDataPrefix();

    /**
     * If this property is non-null, only the properties of Scene/Node that start with this prefix will be exported, and the prefix will be removed.
     * @param value New value
     */
    public void setMetaDataPrefix(String value);

    /**
     * Constructor of {@link com.aspose.threed.A3DWSaveOptions}
     */
    public A3DWSaveOptions();
}

{{< /highlight >}}

Il nuovo A3DWSaveOptions consente di esportare le informazioni e le proprietà delle risorse in un file A3DW.

Viene utilizzato con il nostro nuovo renderer Web in arrivo.

{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Pyramid()).setProperty("rvm:No", "347923");
    var opt = new A3DWSaveOptions();
    opt.setMetaDataPrefix("rvm:");
    scene.save("test.a3dw", opt);

{{< /highlight >}}
