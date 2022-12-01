---
title: Aspose.3D for Java 20,10 Utgivning
type: docs
weight: 7
url: /sv/java/aspose-3d-for-java-20-10-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 20.10.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-737 |Lägg till primitivt stöd i A3DW export/import.|
|THREEDNET-732 |Aspose.3D har ett texturfel vid generering GLTF, men det finns inga problem med att spara det som FBX|
|THREEDNET-738 |Lägg till färgtabellstöd i RVM fil.|
|THREEDNET-739 |Stöd till 7.7/Binary/Autodesk FBX|


## API ändringar ##

### Lagt till nya filformat till klass com.aspose.3reed.FileFormat:

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

Nu kan du exportera scenen till FBX 7.6/7.7 i ASCII/Binläge.

Provkod:

{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Pyramid());
    scene.save("fbx7.7.fbx", FileFormat.FBX7700_BINARY);

{{< /highlight >}}


### Lagt till ny klass com.aspose.tre.A3DWSaveOptions.

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

Den nya A3DWSaveOptions kan du exportera tillgång info och egenskaper till A3DW fil.

Detta används med vår nya inkommande webben renderare.

{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Pyramid()).setProperty("rvm:No", "347923");
    var opt = new A3DWSaveOptions();
    opt.setMetaDataPrefix("rvm:");
    scene.save("test.a3dw", opt);

{{< /highlight >}}
