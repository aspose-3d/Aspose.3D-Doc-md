---
title: Aspose.3D for .NET 18.1-Gennaio 2018
type: docs
weight: 120
url: /it/net/aspose-3d-for-net-18-1-january-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.1](https://www.nuget.org/packages/Aspose.3D/18.1.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-331|Aggiungi nuova entità-Supporto torus rettangolare|Nuova funzionalità|
|THREEDNET-323|Importazione di un documento ASE|Nuova funzionalità|
|THREEDNET-327|Trasformata non valida per il file RVM con più primitive nello stesso nodo.|Bug|
|THREEDNET-325|Il file RVM con cilindro inclinato non è supportato.|Bug|
|THREEDNET-324|Impossibile importare un file RVM|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge ASE membri alla classe Aspose.ThreeD.FileFormat**
Viene utilizzato per identificare il formato di input del file durante il caricamento di una scena dal flusso o dal nome del file.

**C#**

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.FileFormat ASE;

{{< /highlight >}}

{{% alert color="primary" %}} 

Aspose.3D può auto rilevare se il tipo di un file è ASE o altri formati, questo di solito non è necessario quando si chiama Scene.Open metodo.

{{% /alert %}} 

**Codice campione**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.ase", FileFormat.ASE);

{{< /highlight >}}
#### **Aggiunge la proprietà CenterScene alla classe Aspose.ThreeD.A3DObject**
Il valore predefinito è falso, se questo è vero, lo Aspose.3D API proverà a centrare la scena spostando il nodo radice.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.rvm", new RvmLoadOptions() {CenterScene = true});

{{< /highlight >}}
#### **Aggiunge una nuova classe Aspose.ThreeD.Entities.RectangularTorus**
Consente all'utente di posizionare un toro rettangolare parametrizzato nella scena, questo può essere convertito in mesh/mesh triangolare ordinale durante il salvataggio della scena in diversi formati di file supportati.

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Parameterized rectangular torus.

/// </summary>

public class RectangularTorus : Primitive

{

    /// <summary>

    /// The inner radius of the rectangular torus

    /// Default value is 17

    /// </summary>

    public double InnerRadius { get; set; }

    /// <summary>

    /// The outer radius of the rectangular torus

    /// Default value is 20

    /// </summary>

    public double OuterRadius { get; set; }

    /// <summary>

    /// The height of the rectangular torus.

    /// Default value is 20

    /// </summary>

    public double Height { get; set; }

    /// <summary>

    /// The total angle of the arc, measured in radian.

    /// Default value is PI

    /// </summary>

    public double Arc { get; set; }

    /// <summary>

    /// The start angle of the arc, measured in radian.

    /// Default value is 0

    /// </summary>

    public double AngleStart { get; set; }

    /// <summary>

    /// The radial segments, default value is 10

    /// </summary>

    public int RadialSegments { get; set; }

    /// <summary>

    /// Constructor of <see cref="RectangularTorus"/>

    /// </summary>

    public RectangularTorus();

    /// <summary>

    /// Constructor of <see cref="RectangularTorus"/>

    /// </summary>

    public RectangularTorus(string name);

    /// <summary>

    /// Convert this primitive to <see cref="Mesh"/>

    /// </summary>

    /// <returns></returns>

    public Mesh ToMesh();

}

{{< /highlight >}}

**Codice del campione:**

**C#**

{{< highlight "java" >}}

 RectangularTorus rt = new RectangularTorus();

rt.InnerRadius = 17;

rt.OuterRadius = 22;

rt.Height = 30;

rt.Arc = Math.PI * 0.5;

Scene scene = new Scene();

scene.RootNode.CreateChildNode(rt);

scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Il rtorus.obj generato assomiglia a:

![Todo: immagine_Alt_Testo](aspose-3d-for-net-18-1-january-2018_1.png)
#### **Esempi di utilizzo**
Controlla l'elenco degli argomenti di aiuto aggiunti o aggiornati nei documenti Wiki Aspose.3D:

1. [Creare e leggere una scena esistente 3D](/3d/it/net/create-and-read-an-existing-3d-scene/)
1. [Creare Torus rettangolare nella scena 3D](/3d/it/net/create-rectangular-torus-in-3d-scene/)
