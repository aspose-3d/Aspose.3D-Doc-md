---
title: Aspose.3D for .NET 17.4.0 Note di rilascio
type: docs
weight: 90
url: /it/net/aspose-3d-for-net-17-4-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 17.4.0](https://www.nuget.org/packages/Aspose.3D/17.4.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-235|Aggiungere il supporto per l'esportazione di modelli 3D al formato Google Draco (.drc).|Nuova funzionalità|
|THREEDNET-237|Migliorare il movimento della fotocamera in modalità di proiezione ortografica.|Miglioramento|
|THREEDNET-238|Aggiungi supporto per ridurre lo zoom della fotocamera|Miglioramento|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Salvataggio di un modello 3D nel formato Google Draco (.drc)**
La recente versione di Aspose.3D for .NET API ha aggiunto il supporto per l'esportazione di modelli 3D nei formati Google Draco (.drc). Gli sviluppatori possono importare qualsiasi file 3D supportato e quindi salvare in un formato Google Draco.

Questo esempio di codice mostra come esportare un modello 3D in un formato di file Google Draco:

**.NET, C#**

{{< highlight "java" >}}

 //Create a new scene

var s = new Scene();

//Create a sphere object and attach it to the scene

s.RootNode.CreateChildNode("sphere", new Sphere());

//save it to file using draco format

s.Save("sphere.drc", FileFormat.Draco);

{{< /highlight >}}
#### **Aggiunge Aspose.ThreeD.Formats.Draco.DracoCompressionLevel Enum**
DracoCompressionLevel Enum aiuta a definire un livello di compressione prima di salvare un modello 3D nel formato Google Draco (.drc).

Il seguente codice completo dell'Enum mostra vari livelli di compressione con descrizione:

**.NET, C#**

{{< highlight "java" >}}

 public enum DracoCompressionLevel

{

    /// <summary>

    /// No compression, this will result in the minimum encoding time.

    /// </summary>

    NoCompression,

    /// <summary>

    /// Encoder will perform a compression as quickly as possible.

    /// </summary>

    Fast,

    /// <summary>

    /// Standard mode, with good compression and speed.

    /// </summary>

    Standard,

    /// <summary>

    /// Encoder will compress the scene optimally, which may takes longer time to finish.

    /// </summary>

    Optimal

}

{{< /highlight >}}
### **Aggiunge Aspose.ThreeD.Formats.Draco.DracoSaveOptions Classe**
La classe DracoSaveOptions consente agli sviluppatori di applicare le impostazioni prima di salvare un modello 3D nel formato Google Draco (.drc).

Il seguente codice completo della classe mostra tutte le proprietà con descrizione:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Quantization bits for position

/// </summary>

public int PositionBits { get; set; }

/// <summary>

/// Quantization bits for texture coordinate

/// </summary>

public int TextureCoordinateBits { get; set; }

/// <summary>

/// Quantization bits for vertex color

/// </summary>

public int ColorBits { get; set; }

/// <summary>

/// Quantization bits for normal vectors

/// </summary>

public int NormalBits { get; set; }

/// <summary>

/// Compression level

/// </summary>

public DracoCompressionLevel CompressionLevel { get; set; }

{{< /highlight >}}
#### **Aggiunge Aspose.ThreeD.Formats.DracoFormat Class**
Questo**Codifica**Il metodo della classe DracoFormat consente agli sviluppatori di codificare una singola mesh invece dell'intera scena, il che è più efficiente.

Il seguente codice completo della classe mostra il metodo Encode con descrizione:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Encode the mesh to Draco mesh raw data

/// </summary>

/// <param name="mesh"></param>

/// <param name="options"></param>

/// <returns></returns>

public byte[]Encode(IMeshConvertible mesh, DracoSaveOptions options = null);

{{< /highlight >}}
#### **Codificare una mesh nel formato Google Draco (.drc)**
Il file Draco non ha il supporto per la scena gerarchica, ciascuno. Il file drc rappresenta una mesh, quindi il salvataggio della scena unirà l'intera scena in una singola mesh, il che potrebbe perdere informazioni.

Questo esempio di codice mostra come codificare una mesh nel formato Google Draco (.drc):

**.NET, C#**

{{< highlight "java" >}}

 //Create a sphere

var mesh = new Sphere();

// Encode the sphere to Google Draco raw data using optimal compression level.

var b = FileFormat.Draco.Encode(mesh,

    new DracoSaveOptions() {CompressionLevel = DracoCompressionLevel.Optimal});

//Save the raw bytes to file

File.WriteAllBytes("sphere.drc", b);

{{< /highlight >}}
#### **Aggiunge il membro della modalità di rotazione alla classe Aspose.ThreeD.Entities.Frustum (classe base della fotocamera e della luce)**
Il valore predefinito è RotationMode.FixedTarget, lo rende compatibile con il vecchio codice nel rendering in tempo reale. Se la modalità di rotazione di Frustum è FixedTarget, l'orientamento del frustum è specificato dalla sua proprietà LookAt che è una posizione assoluta nello spazio mondiale, in questa modalità gli sviluppatori possono sempre ottenere proprietà di direzione diverse quando la sua posizione viene cambiata.

Se la modalità di rotazione è FixedDirection, il frustum non guarderà più un bersaglio, ma manterrà la stessa direzione (specificata dalla sua proprietà Direction) rispetto alla sua posizione, questo è utile nella progettazione di strumenti come CAD o FPS game, in questa modalità gli sviluppatori possono sempre ottenere diverse proprietà LookAt quando la sua posizione viene modificata.

Questo esempio di codice dimostra come impostare la modalità di rotazione di una fotocamera:

**.NET, C#**

{{< highlight "java" >}}

 Camera camera = new Camera();

camera.RotationMode = RotationMode.FixedDirection;

{{< /highlight >}}
#### **Aggiunge il membro di ingrandimento a Aspose.ThreeD. Entità. Classe di fotocamera**
Il valore predefinito è (1, 1), modificare questo valore può rendere le scale dell'immagine renderizzata in direzione orizzontale/verticale nella fotocamera ortografica.

Questo esempio di codice dimostra come impostare la modalità di rotazione di una fotocamera:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the magnification used in orthographic camera

/// </summary>

public Vector2 Magnification { get;set; }

.................................................

Camera camera = new Camera();

camera.Magnification = new Vector2(2, 2);

{{< /highlight >}}
