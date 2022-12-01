---
title: Aspose.3D for .NET 17.5 Note di rilascio
type: docs
weight: 80
url: /it/net/aspose-3d-for-net-17-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 17.5](https://www.nuget.org/packages/Aspose.3D/17.5.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-244|Nuovo materiale PBR per supportare il rendering basato fisicamente|Nuova funzionalità|
|THREEDNET-250|Consentire agli Aspose.3D API di importare i file GLTF 2.0 ASCII|Nuova funzionalità|
|THREEDNET-253|Consentire agli Aspose.3D API di importare i file binari GLTF 2.0|Nuova funzionalità|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge Aspose.ThreeD.Shading.PbrMaterial Class**
La recente versione di Aspose.3D for .NET API ha aggiunto il supporto del materiale PBR (Physically Based Rendering). Gli sviluppatori possono applicare materiale PBR alle entità e eseguire il rendering nei modelli 3D.

Questo esempio di codice mostra come applicare il materiale PBR a un'entità:

**.NET, C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

PbrMaterial mat = new PbrMaterial();

mat.MetallicFactor = 0.9;//an almost metal material

mat.RoughnessFactor = 0.9;//material surface is very rough

//create a box that applied this material

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

{{< /highlight >}}
#### **Aggiornamenti dei membri allo Aspose.ThreeD. Classe FileFormat**
Per importare i file GLTF 2.0 (ASCII & Binary) in Aspose.3D API, due membri (GLTF2 & GLTF2 _ Binary) vengono aggiunti allo Aspose.ThreeD.

Questo esempio di codice dimostra come importare GLTF 2.0 ASCII o file binario:

**.NET, C#**

{{< highlight "java" >}}

 /********************** New Members **********************/

public static readonly Aspose.ThreeD.FileFormat GLTF2;

public static readonly Aspose.ThreeD.FileFormat GLTF2_Binary;



/******************** Import GLTF 2.0 ********************/

//Create a new scene

var s = new Scene();

//Load it as GLTF2, the second argument is optional since Aspose.3D can detect the actual file type

s.Open("test.gltf", FileFormat.GLTF2);

{{< /highlight >}}

