---
title: Aspose.3D for Java 18.11-Novembre 2018
type: docs
weight: 20
url: /it/java/aspose-3d-for-java-18-11-november-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per Aspose.3D for Java 18.11.

{{% /alert %}} 
## **Miglioramenti e modifiche**


|**Riassunto**|**Categoria**|
|:- |:- |
|Problema con la proprietà UnitScaleFactor|Bug|
|Problema con le texture incorporate|Bug|

## **Pubblico API e modifiche incompatibili arretrate**
Si prega di visualizzare l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché eventuali modifiche non retrocompatibili apportate allo Aspose.3D for Java API. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).

## **API modifiche:**

**Aggiunti membri alla classe "com.aspose.threed.FBXSaveOptions":**

{{< highlight "java" >}}

     /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public boolean com.aspose.threed.FBXSaveOptions.getEnableCompression();

    /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public void com.aspose.threed.FBXSaveOptions.setEnableCompression(boolean val);

{{< /highlight >}}





**Codice del campione:**

{{< highlight "java" >}}

     Scene scene = new Scene("test.fbx");

    FBXSaveOptions opts = new FBXSaveOptions(FileFormat.FBX7500_BINARY);

    opts.setEnableCompression(false);

    scene.save("test.fbx", opts);

{{< /highlight >}}
