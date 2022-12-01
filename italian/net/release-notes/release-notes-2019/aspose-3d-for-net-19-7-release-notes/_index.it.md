---
title: Aspose.3D for .NET 19.7 Note di rilascio
type: docs
weight: 60
url: /it/net/aspose-3d-for-net-19-7-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 19.7](https://www.nuget.org/packages/Aspose.3D/19.7.0)

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-449|Problema con i valori di trasformazione nei nodi|Caratteristica|
|THREEDNET-526|Aggiungi supporto per l'esportazione di punti cloud nel Google Draco|Miglioramento|
|THREEDNET-524|Aggiungi il supporto per l'importazione di punti cloud nel Google Draco|Miglioramento|
|THREEDNET-523 |Aggiungi supporto point cloud nel formato PLY|Miglioramento|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **Aggiunta nuova classe Aspose.ThreeD.Entities.PointCloud**
Questa classe eredita da Aspose.ThreeD. Entità. Geometria direttamente e utilizzata per rappresentare un insieme di punti.
### **Aggiunti nuovi metodi Decodifica alla classe Aspose.ThreeD.Formats.DracoFormat**
{{< highlight "java" >}}

 /// <summary>

/// Decode the point cloud or mesh from specified file name

/// </summary>

/// <param name="fileName">The file name contains the drc file</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance depends on the file content</returns>

public Geometry Decode(string fileName);

/// <summary>

/// Decode the point cloud or mesh from memory data

/// </summary>

/// <param name="data">The raw drc bytes</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance depends on the content</returns>

public Geometry Decode(byte[]data)

{{< /highlight >}}

Codice di esempio per decodificare direttamente una mesh da un file draco senza creare una scena

{{< highlight "java" >}}

 var pointCloud = (PointCloud) FileFormat.Draco.Decode("pointCloud.drc");

{{< /highlight >}}
### **Aggiunti nuovi metodi Codificare alla classe Aspose.ThreeD.Formats.DracoForma**
{{< highlight "java" >}}

 /// <summary>

/// Encode the entity to specified stream

/// </summary>

/// <param name="entity">The entity to be encoded</param>

/// <param name="stream">The stream that encoded data will be written to</param>

/// <param name="options">Extra options for encoding the point cloud</param>

public void Encode(Entity entity, Stream stream, DracoSaveOptions options = null);

/// <summary>

/// Encode the entity to specified file

/// </summary>

/// <param name="entity">The entity to be encoded</param>

/// <param name="fileName">The file name to be written</param>

/// <param name="options">Extra options for encoding the point cloud</param>

public void Encode(Entity entity, string fileName, DracoSaveOptions options = null);

/// <summary>

/// Encode the entity to Draco raw data

/// </summary>

/// <param name="entity">The entity to be encoded</param>

/// <param name="options">Extra options for encoding the point cloud</param>

/// <returns>The encoded draco data represented in bytes</returns>

public byte[]Encode(Entity entity, DracoSaveOptions options = null);

{{< /highlight >}}

Codice di esempio per codificare direttamente una mesh sfera in file draco senza costruire una scena

{{< highlight "java" >}}

 FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
### **Aggiunti nuovi metodi PointCloud alla classe Aspose.ThreeD.Formats.DracoSaveOptions**
{{< highlight "java" >}}

 /// <summary>

/// Export the scene as point cloud, default value is false.

/// </summary>

public bool PointCloud { get; set; } 

{{< /highlight >}}

Codice di esempio per codificare una mesh a sfera in file draco come nuvola di punti

{{< highlight "java" >}}

 FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() {PointCloud = true});

{{< /highlight >}}
### **Aggiunti nuovi metodi Codificare alla classe Aspose.ThreeD.Formats.PlyFormat**
{{< highlight "java" >}}

 /// <summary>

/// Encode the entity and save the result into the stream.

/// </summary>

/// <param name="entity">The entity to encode</param>

/// <param name="stream">The stream to write to, this method will not close this stream</param>

/// <param name="opt">Save options</param>

public void Encode(Entity entity, Stream stream, PlySaveOptions opt = null);

/// <summary>

/// Encode the entity and save the result into an external file.

/// </summary>

/// <param name="entity">The entity to encode</param>

/// <param name="fileName">The file to write to</param>

/// <param name="opt">Save options</param>

public void Encode(Entity entity, string fileName, PlySaveOptions opt = null);

{{< /highlight >}}

Codice di esempio per codificare una mesh per inserire direttamente il file senza creare una scena.

{{< highlight "java" >}}

 FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
### **Aggiunti nuovi metodi Decodifica alla classe Aspose.ThreeD.Formats.PlyFormat**
{{< highlight "java" >}}

 /// <summary>

/// Decode a point cloud or mesh from the specified stream.

/// </summary>

/// <param name="fileName">The input stream</param>

/// <param name="opt">The load option of PLY format</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance</returns>

public Geometry Decode(string fileName, PlyLoadOptions opt = null);

/// <summary>

/// Decode a point cloud or mesh from the specified stream.

/// </summary>

/// <param name="stream">The input stream</param>

/// <param name="opt">The load option of PLY format</param>

/// <returns>A <see cref="Mesh"/> or <see cref="PointCloud"/> instance</returns>

public Geometry Decode(Stream stream, PlyLoadOptions opt = null);

{{< /highlight >}}

Codice di esempio per decodificare una nuvola mesh/point da un file ply:

{{< highlight "java" >}}

 var geom = FileFormat.PLY.Decode("sphere.ply");

{{< /highlight >}}
### **Aggiunta la proprietà PointCloud alla classe Aspose.ThreeD.Formats.PlySaveOptions**
{{< highlight "java" >}}

 /// <summary>

/// Export the scene as point cloud, the default value is false.

/// </summary>

public bool PointCloud { get; set; }

{{< /highlight >}}

Codice di esempio per forzare l'esportazione di una scena come nuvola di punti

{{< highlight "java" >}}

 FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions(){PointCloud = true});

{{< /highlight >}}
