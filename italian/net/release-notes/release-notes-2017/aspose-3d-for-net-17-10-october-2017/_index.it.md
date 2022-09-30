---
title: Aspose.3D for .NET 17.10-Ottobre 2017
type: docs
weight: 30
url: /it/net/aspose-3d-for-net-17-10-october-2017/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 17.10](https://www.nuget.org/packages/Aspose.3D/17.10.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-292|Aggiungere il supporto per l'importazione 3MF|Nuova funzionalità|
|THREEDNET-302|OBJ allo GLTF-rendering incompleto del modello 3D|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge il membro Microsoft3MF alle classi Aspose.ThreeD.FileFormat e Aspose.ThreeD.FileFormatType**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Microsoft 3D Manufacturing Format

/// </summary>

public static readonly Aspose.ThreeD.FileFormat Microsoft3MF;



/// <summary>

/// Microsoft 3D Manufacturing Format

/// </summary>

public static readonly Aspose.ThreeD.FileFormatType Microsoft3MF;

{{< /highlight >}}

Il rilevamento automatico del formato è supportato per il file 3MF, quindi gli sviluppatori possono importarlo direttamente con il costruttore della classe Scene senza specificare esplicitamente FileFormat.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene("sphere_logo.3mf");

{{< /highlight >}}
