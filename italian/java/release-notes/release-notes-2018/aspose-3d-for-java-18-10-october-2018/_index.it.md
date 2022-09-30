---
title: Aspose.3D for Java 18.10-ottobre 2018
type: docs
weight: 30
url: /it/java/aspose-3d-for-java-18-10-october-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 18.10](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.10/).

{{% /alert %}} 
## **Miglioramenti e modifiche**


|**Riassunto**|**Categoria**|
|:- |:- |
|Supporto for .NET piattaforma Core|Nuova funzione|
|Consentire all'utente di disattivare la compressione quando si salvano i file binari FBX|Nuova funzione|
|Migliorare le prestazioni delle importazioni FBX|Miglioramento|
|Migliorare FBX Prestazioni binarie di scrittura|Miglioramento|
|Eccezione di importanza durante l'apertura di enormi file FBX|Bug|
|Problema con la proprietà UnitScaleFactor|Bug|

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
