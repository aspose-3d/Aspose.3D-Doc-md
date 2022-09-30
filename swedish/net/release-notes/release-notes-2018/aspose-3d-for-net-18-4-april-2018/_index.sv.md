---
title: Aspose.3D for .NET 18,4 – april 2018
type: docs
weight: 90
url: /sv/net/aspose-3d-for-net-18-4-april-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 18,4](https://www.nuget.org/packages/Aspose.3D/18.4.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-376|Lägg till huden controller export stöd i Collada|Ny funktion|
|THREEDNET-377|Lägg till stöd för egenskaper animation i Collada exportering|Ny funktion|
|THREEDNET-373|Lägg till stöd för animation i Collada importering|Ny funktion|
|THREEDNET-375|Lägg till huden controller import stöd i Collada|Ny funktion|
|THREEDNET-349|Collada saknas Material ID|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
### **API ändringar**
De nya funktionerna (Collada animation importerar och exporterar) 18.4 inför inte API förändringar.

De API förändringarna i 18,4 är i två kategorier:

1. För konsekvens enligt Aspose.3D for Java API
1. Avskaffade föråldrade metoder
#### **SetData och SetIndices metoder till Aspose.ThreeD.Enheter.VertexElement klass**
**Definition - C#**

{{< highlight "java" >}}

 /// <summary>

/// Load data

/// </summary>

/// <param name="data"></param>

public void SetData([]data);

/// <summary>

/// Load indices

/// </summary>

/// <param name="data"></param>

public void SetIndices(int[]data);

{{< /highlight >}}

De nya metoderna används för att hålla API överensstämmande mellan Aspose.3D for Java och Aspose.3D 1 for .NET:

**Kodexempel - C#**

{{< highlight "java" >}}

 //Modified from https://github.com/aspose-3d/Aspose.3D-for-.NET/blob/master/Examples/CSharp/Geometry-and-Hierarchy/SetupUVOnCube.cs

// UVs

Vector4[]uvs = new Vector4[]{

    new Vector4( 0.0, 1.0,0.0, 1.0),

    new Vector4( 1.0, 0.0,0.0, 1.0),

    new Vector4( 0.0, 0.0,0.0, 1.0),

    new Vector4( 1.0, 1.0,0.0, 1.0)

};

// Indices of the uvs per each polygon

int[]uvsId = new int[]{

    0,1,3,2,2,3,5,4,4,5,7,6,6,7,9,8,1,10,11,3,12,0,2,13

};

// Call Common class create mesh using polygon builder method to set mesh instance 

Mesh mesh = Common.CreateMeshUsingPolygonBuilder();

// Create UVset

VertexElementUV elementUV = mesh.CreateElementUV(TextureMapping.Diffuse, MappingMode.PolygonVertex, ReferenceMode.IndexToDirect);

// Copy the data to the UV vertex element 

elementUV.SetData(uvs); //Equivalent to elementUV.Data.AddRange(uvs);

elementUV.SetIndices(uvsId); // Equivalent to elementUV.Indices.AddRange(uvsId);

{{< /highlight >}}
#### **Lägger till ChildNode metod till Aspose.ThreeD.Nod klass**
**Definition - C#**

{{< highlight "java" >}}

 /// <summary>

/// Add a child node to this node

/// </summary>

/// <param name="node">The child node to be attached</param>

public void AddChildNode(Aspose.ThreeD.Node node);

{{< /highlight >}}

**Kod Exempel - C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

Node newChild = new Node();

scene.RootNode.AddChildNode(newChild); // Equivalent to scene.RootNode.ChildNodes.Add(newChild);

{{< /highlight >}}


#### **Lägger AddElement metod till Aspose.ThreeD.Enheter.Geometri klass**
**Definition - C#**

{{< highlight "java" >}}

 /// <summary>

/// Adds an existing vertex element to current geometry

/// </summary>

/// <param name="element">The vertex element to add</param>

public void AddElement(Aspose.ThreeD.Entities.VertexElement element);

{{< /highlight >}}

De nya metoderna används för att hålla API överensstämmande mellan Aspose.3D for Java och Aspose.3D 1 for .NET API:

**Kodexempel - C#**

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

VertexElement uv = new VertexElementUV();

mesh.AddElement(uv);

{{< /highlight >}}
#### **Tar bort GetControlPointIndex från Aspose.ThreeD.Entiteter.**
**Definition - C#**

{{< highlight "java" >}}

 public int GetControlPointIndex(int u, int v)

{{< /highlight >}}
#### **Ta bort Ladda, Spara och ToBitmap metoder från Aspose.ThreeD.Render.ITextureUnit klass**
Dessa metoder markerades som föråldrade i version 17.8, motsvarande ersättningar finns i de härledda gränssnitten ITexture1D/ITexture2D/ITextureCubemap.

**Definition - C#**

{{< highlight "java" >}}

 public void Load(Aspose.ThreeD.Render.TextureData bitmap)

public void Save(string path, System.Drawing.Imaging.ImageFormat format)

public void Save(System.Drawing.Bitmap bitmap)

public System.Drawing.Bitmap ToBitmap()

{{< /highlight >}}
