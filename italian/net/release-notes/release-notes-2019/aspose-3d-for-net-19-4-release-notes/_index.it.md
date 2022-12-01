---
title: Aspose.3D for .NET 19.4 Note di rilascio
type: docs
weight: 90
url: /it/net/aspose-3d-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 19.4](https://www.nuget.org/packages/Aspose.3D/19.4.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-471|XPath come metodi di indirizzamento degli oggetti|Nuova funzionalità|
|THREEDNET-483|Supporto per il formato VRML|Nuova funzionalità|
|THREEDNET-493|Aggiunto il supporto del renderer Vulkan nella versione Core .NET|Nuova funzionalità|
|THREEDNET-496|Problema di corruzione delle esportazioni FBX7500Binarie|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
#### **Aggiunto raggio di nuova proprietà nella classe Aspose.ThreeD.Entities.Sphere**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the radius of the sphere.

/// </summary>

public double Radius { get; set; }

{{< /highlight >}}

Codice di esempio per specificare il raggio per proprietà piuttosto che l'argomento del costruttore:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode(new Sphere() {Radius = 10});

scene.Save("sphere.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Aggiunto nuovo formato di file VRML in classe Aspose.ThreeD.FileFormat e Aspose.ThreeD.FileFormatType**
{{< highlight "java" >}}

 /// <summary>

/// The Virtual Reality Modeling Language

/// </summary>

public static readonly FileFormat VRML;

{{< /highlight >}}

Aspose.3D può rilevare automaticamente il formato VRML, quindi il FileFormat viene solitamente ignorato nel metodo Open. Codice del campione:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.wrl");

{{< /highlight >}}
