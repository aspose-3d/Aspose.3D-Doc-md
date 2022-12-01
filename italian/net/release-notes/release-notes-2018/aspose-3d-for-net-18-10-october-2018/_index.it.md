---
title: Aspose.3D for .NET 18.10-ottobre 2018
type: docs
weight: 30
url: /it/net/aspose-3d-for-net-18-10-october-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.10](https://www.nuget.org/packages/Aspose.3D/18.10.0).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-434|Supporto for .NET piattaforma Core|Nuova funzione|
|THREEDNET-431|Consentire all'utente di disattivare la compressione quando si salvano i file binari FBX|Nuova funzione|
|THREEDNET-424|Migliorare le prestazioni delle importazioni FBX|Miglioramento|
|THREEDNET-432|Migliorare FBX Prestazioni binarie di scrittura|Miglioramento|
|THREEDNET-428|Eccezione di importanza durante l'apertura di enormi file FBX|Bug|
|THREEDNET-429|Problema con la proprietà UnitScaleFactor|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **API modifiche**
#### **Membri aggiunti alla classe Aspose.ThreeD.Formats.FBXSaveOptions:**
{{< highlight "java" >}}

         /// <summary>

        /// Compression large binary data in the FBX file, default value is true.

        /// </summary>

        public bool EnableCompression{ get;set;}

{{< /highlight >}}

**Codice del campione:**

{{< highlight "java" >}}

         Scene scene = new Scene("test.fbx");

        scene.Save("test.fbx", new FBXSaveOptions(FileFormat.FBX7500ASCII) {EnableCompression = false});

{{< /highlight >}}
