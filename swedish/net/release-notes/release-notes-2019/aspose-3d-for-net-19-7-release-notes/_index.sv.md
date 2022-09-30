---
title: Aspose.3D for .NET 19,7 Utgivning
type: docs
weight: 60
url: /sv/net/aspose-3d-for-net-19-7-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,7](https://www.nuget.org/packages/Aspose.3D/19.7.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-449|Problem med transformationsvärden i Noder|Funktion|
|THREEDNET-526|Lägg till punkt moln exportstöd Google Draco|Förbättring|
|THREEDNET-524|Lägg till stöd för molnimport i Google Draco|Förbättring|
|THREEDNET-523 |Lägg till stöd för punkt moln i PLY format|Förbättring|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **Tillagd ny klass Aspose.ThreeD.Enheter.PointCloud.**
Denna klass ärver från Aspose.ThreeD.Enheter.Geometri direkt och används för att representera en uppsättning poäng.
### **Lagt till nya metoder Avkoda till klass Aspose.ThreeD.Formats.DracoFormatt**
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

Provkod för att avkoda en mesh från en draco-fil direkt utan att bygga en scen.

{{< highlight "java" >}}

 var pointCloud = (PointCloud) FileFormat.Draco.Decode("pointCloud.drc");

{{< /highlight >}}
### **Lagt till nya metoder koda till klass Aspose.ThreeD.Formats.DracoForma.**
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

Provkod för att koda ett sfärsnät till draco-fil direkt utan att bygga en scenn

{{< highlight "java" >}}

 FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
### **Lagt till nya metoder PointCloud till klass Aspose.ThreeD.Formats.DracoSaveOptioner**
{{< highlight "java" >}}

 /// <summary>

/// Export the scene as point cloud, default value is false.

/// </summary>

public bool PointCloud { get; set; } 

{{< /highlight >}}

Provkod för att koda ett sfärsnät till draco-filen som ett punktmoln

{{< highlight "java" >}}

 FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() {PointCloud = true});

{{< /highlight >}}
### **Lagt till nya metoder koda till klass Aspose.ThreeD.Formats.PlyFormat.**
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

Provkod för att koda en mesh för att ply filen direkt utan att bygga en scen.

{{< highlight "java" >}}

 FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
### **Lagt till nya metoder Avkoda till klass Aspose.ThreeD.Format.PlyFormat.**
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

Provkod för att avkoda ett nät/punktmoln från en lagfil:

{{< highlight "java" >}}

 var geom = FileFormat.PLY.Decode("sphere.ply");

{{< /highlight >}}
### **Tillagd egenskap PointCloud till klass Aspose.ThreeD.Formats.PlySaveOptions**
{{< highlight "java" >}}

 /// <summary>

/// Export the scene as point cloud, the default value is false.

/// </summary>

public bool PointCloud { get; set; }

{{< /highlight >}}

Samplingskod för att tvinga att exportera en scen att spela som punktmoln

{{< highlight "java" >}}

 FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions(){PointCloud = true});

{{< /highlight >}}
