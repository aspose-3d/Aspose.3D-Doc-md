---
title: Aspose.3D for .NET 19,10 Utgivningsmeddelanden
type: docs
weight: 30
url: /sv/net/aspose-3d-for-net-19-10-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgivningsanmärkningar för Aspose.3D for .NET 19.10.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-567 |` `Problem konvertering RVM & ATT bricka|Förbättring|
|THREEDNET-570 |` `Beräkning av avgränsande låda av primitiva former är felaktig|Förbättring|
|THREEDNET-571 |` `Export primitiva former till RVM fil.|Förbättring|
|THREEDNET-572 |` `Förbättra det primitiva exportstödet under FBX.|Förbättring|
|THREEDNET-573 |` `Speciella tecken i objektnamn kan inte exporteras korrekt i FBX format.|FelComment|
|THREEDNET-568 |` ` Sparat. Gb- filer kan inte öppnas.|FelComment|
|THREEDNET-549|Att lasta enorm RVM tar mycket tid och resurser|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **Ny klass - Aspose.ThreeD.**
Detta är en ny parameteriserad primitiv form.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("dish", new Dish(), new PbrMaterial(Color.Coral));

{{< /highlight >}}
### **Ny klass - Aspose.ThreeD.Enheter.Pyramid**
Detta är en ny parameteriserad primitiv form.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("pyramid", new Pyramid(), new PbrMaterial(Color.Coral));

{{< /highlight >}}
### **Nya egenskaper inkom i klass Aspose.ThreeD.Enheter.Box**


Följande egenskaper har lagts till i Aspose.ThreeD Enheter.Box-klass.

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the length segments.

/// </summary>

public int LengthSegments{ get;set;}

/// <summary>

/// Gets or sets the width segments

/// </summary>

public int WidthSegments{ get;set;}

/// <summary>

/// gets or sets the height segments.

/// </summary>

public int HeightSegments{ get;set;}

{{< /highlight >}}
### **Avlägsnad metod HittaNode i klass Aspose.ThreeD.Node**
Detta var planerat att tas bort eftersom det har ersatts av mer avancerade SelectSingleObject/Select Objekt.
### **Ny metod lagts till Aspose.ThreeD.Node**
Följande metod har lagts till Aspose.ThreeD.Nod klass som gör det mer bekvämt att skapa en nod med en Material.

{{< highlight "java" >}}

 /// <summary>

/// Create a new child node with given node name, and attach specified entity and a material

/// </summary>

/// <param name="nodeName">The new child node's name</param>

/// <param name="entity">Default entity attached to the node</param>

/// <param name="material">The material attached to the node</param>

/// <returns>The new child node.</returns>

public Node CreateChildNode(string nodeName, Entity entity, Material material);

{{< /highlight >}}

Urvalskod

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("box", new Box(), new PbrMaterial(Color.Coral));

{{< /highlight >}}

Avlägsnade metoder från klass Aspose.ThreeD.Format.PlyFormat

Följande metoder har ersatts av PlyFormat.Encode som också kan användas för att koda punktmoln.



{{< highlight "java" >}}

 public void EncodeMesh(Aspose.ThreeD.Entities.IMeshConvertible mesh, System.IO.Stream stream, Aspose.ThreeD.Formats.PlySaveOptions opt);

public void EncodeMesh(Aspose.ThreeD.Entities.IMeshConvertible mesh, string fileName, Aspose.ThreeD.Formats.PlySaveOptions opt);

{{< /highlight >}}

Lagt till ny egenskap i klass Aspose.ThreeD.Formats.FBXSaveOptions.

Denna egenskap gör det praktiskt att exportera stora scener som består av primitiva.



{{< highlight "java" >}}

 /// <summary>

/// Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

/// Default value is false

/// </summary>

public bool ReusePrimitiveMesh { get; set; }

{{< /highlight >}}
#### **Urvalskod**
{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("dish A", new Dish(), new PbrMaterial(Color.Coral));

scene.RootNode.CreateChildNode("dish B", new Dish(), new PbrMaterial(Color.Coral));

scene.Save("file.fbx", new FBXSaveOptions(FileFormat.FBX7400ASCII) { ReusePrimitiveMesh = true });

{{< /highlight >}}



Eftersom de två parameteriserade formerna har samma parametrar, kommer de definitivt generera samma mesh. När denna egenskap är sann, kommer den genererade FBX filen bara generera en mesh och återanvända den i olika noder.
