---
title: Aspose.3D for .NET Note di rilascio 17.3.0
type: docs
weight: 100
url: /it/net/aspose-3d-for-net-17-3-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 17.3.0](https://www.nuget.org/packages/Aspose.3D/17.3.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-233|Aggiungere il supporto per l'importazione di file Google Draco (.drc).|Nuova funzionalità|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge la voce in formato Draco nella classe Aspose.ThreeD.FileFormat**
Questa versione di Aspose.3D for .NET API ha aggiunto il supporto per l'importazione di file Google Draco(.drc). Gli sviluppatori possono importare un file Google Draco e quindi salvarlo in qualsiasi formato 3D supportato.

Questo esempio di codice dimostra come importare un file Google Draco in Aspose.3D API:

**.NET, C#**

{{< highlight "java" >}}

 // Initialize a Scene class object

Scene scene = new Scene();

// load an existing 3D document

scene.Open("document.drc", FileFormat.Draco);

{{< /highlight >}}
