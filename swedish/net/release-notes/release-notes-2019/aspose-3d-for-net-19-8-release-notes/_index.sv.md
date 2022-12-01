---
title: Aspose.3D for .NET 19,8 Utgivning
type: docs
weight: 50
url: /sv/net/aspose-3d-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,8](/3d/sv/net/aspose-3d-for-net-19-8-release-notes/)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-528|Lägg till stöd för punkt moln i Wavefront OBJ|Ny funktion|
|THREEDNET-531|Säkerhetsgranskning av Aspose.3D|Förbättring|
|THREEDNET-536 |DRC till STL omvandling|FelComment|
|THREEDNET-537|Problem att konvertera PLY till GLB|FelComment|
|THREEDNET-539|Det stora punktmolnet kan generera felaktiga data.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **Lagt ny fastighet PointCloud i klass Aspose.ThreeD.Formats.ObjSparaOptioner**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

/// </summary>

public bool PointCloud

{

    get;set;

}

{{< /highlight >}}

Provkod för att skapa ett punktmoln i Sphere i obj format.

{{< highlight "java" >}}

 var scene = new Scene(new Sphere());

scene.Save(@"sphere.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
### **Lagt till nya metoder CreatePolygon Aspose.ThreeD.Enheter.Mesh**
{{< highlight "java" >}}

 /// <summary>

/// Create a polygon with 4 vertices(quad)

/// </summary>

/// <param name="v1">Index of the first vertex</param>

/// <param name="v2">Index of the second vertex</param>

/// <param name="v3">Index of the third vertex</param>

/// <param name="v4">Index of the fourth vertex</param>

public void CreatePolygon(int v1, int v2, int v3, int v4);

/// <summary>

/// Create a polygon with 3 vertices(triangle)

/// </summary>

/// <param name="v1">Index of the first vertex</param>

/// <param name="v2">Index of the second vertex</param>

/// <param name="v3">Index of the third vertex</param>

public void CreatePolygon(int v1, int v2, int v3);

{{< /highlight >}}

Provkod.

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

mesh.CreatePolygon(new int[]{ 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices

mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

{{< /highlight >}}

De nya metoderna**SkapaPolygonName**Låter dig skapa en triangel eller quad utan att tilldela extra minne, det är mycket optimerat internt.


### **Ta bort gammalt offentligt fält PrettyPrint i klass Aspose.ThreeD.Formats.GLTFSaveOptioner**
Detta togs bort och ersattes av egenskap med samma namn, så äldre kod som använde denna behöver inga ändringar.
### **Lagt till ny egenskap PrettyPrint i klass Aspose.ThreeD.Formats.GLTFSparaOptions**

{{< highlight "java" >}}

 /// <summary>

/// The JSON content of GLTF file is indented for human reading, default value is false

/// </summary>

public bool PrettyPrint { get; set; }

{{< /highlight >}}

Den gamla.**PrettyPrint**Det var ett offentligt fält, och det har ersatts av egendom för konsekvent.
