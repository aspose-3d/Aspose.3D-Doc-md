---
title: Aspose.3D for .NET 19.5 Note di rilascio
type: docs
weight: 80
url: /it/net/aspose-3d-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 19.5](https://www.nuget.org/packages/Aspose.3D/19.5.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-501|Integrare con l'ultimo Dynabic.Metered|Miglioramento|
|THREEDNET-505|Consenti l'orientamento del cambio aereo specificando una normale|Miglioramento|
|THREEDNET-489|Shadow non funziona nel renderer Vulkan|Bug|
|THREEDNET-504|Draco creato dal file STL è rotto|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
#### **Aggiunto raggio di nuova proprietà nella classe Aspose.ThreeD.Entities.Plane**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

/// </summary>

public Vector3 Up { get; set; }

{{< /highlight >}}

Codice di esempio per specificare il raggio per proprietà piuttosto che l'argomento del costruttore:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode(new Plane() {Up = new Vector3(1, 1, 3)});

//This will generate a plane that has customized orientation

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Aggiunto il nuovo metodo "GetConsumptionCredit" nella classe Aspose.ThreeD. Misurato**
{{< highlight "java" >}}

 /// <summary>

/// Gets consumption credit

/// </summary>

/// <returns>consumption quantity</returns>

public static decimal GetConsumptionCredit();

{{< /highlight >}}

` ` Ottiene il credito di consumo del mese corrente, utilizzato dal servizio di fatturazione Dynabic.Metered.
