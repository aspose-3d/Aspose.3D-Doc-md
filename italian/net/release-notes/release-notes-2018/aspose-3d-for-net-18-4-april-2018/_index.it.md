---
title: Aspose.3D for .NET 18.4-Aprile 2018
type: docs
weight: 90
url: /it/net/aspose-3d-for-net-18-4-april-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.4](https://www.nuget.org/packages/Aspose.3D/18.4.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-376|Aggiungi supporto per l'esportazione del controller skin nel Collada|Nuova funzione|
|THREEDNET-377|Aggiungi supporto per l'animazione delle proprietà nell'esportazione dello Collada|Nuova funzione|
|THREEDNET-373|Aggiungi supporto per l'animazione delle proprietà nell'importazione Collada|Nuova funzione|
|THREEDNET-375|Aggiungi il supporto per l'importazione del controller skin nel Collada|Nuova funzione|
|THREEDNET-349|Manca l'ID materiale Collada|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
### **API modifiche**
Le nuove funzionalità (Collada importazione ed esportazione di animazione) in 18.4 non introducono modifiche API.

Le modifiche API in 18.4 sono in due categorie:

1. Per la consistenza nel Aspose.3D for Java API
1. Rimossi metodi obsoleti
#### **Metodi SetData e Setindices fino a Aspose.ThreeD. Classe Entities.VertexElement**
**Definizione-C#**

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

I nuovi metodi aggiunti sono utilizzati per mantenere lo API coerente tra Aspose.3D for Java e Aspose.3D for .NET:

**Esempio di codice-C#**

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
#### **Aggiunge il metodo AddChildNode alla classe Aspose.ThreeD.Node**
**Definizione-C#**

{{< highlight "java" >}}

 /// <summary>

/// Add a child node to this node

/// </summary>

/// <param name="node">The child node to be attached</param>

public void AddChildNode(Aspose.ThreeD.Node node);

{{< /highlight >}}

**Esempio di codice-C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

Node newChild = new Node();

scene.RootNode.AddChildNode(newChild); // Equivalent to scene.RootNode.ChildNodes.Add(newChild);

{{< /highlight >}}


#### **Aggiunge il metodo di aggiunta a Aspose.ThreeD. Entità. Classe di geometria**
**Definizione-C#**

{{< highlight "java" >}}

 /// <summary>

/// Adds an existing vertex element to current geometry

/// </summary>

/// <param name="element">The vertex element to add</param>

public void AddElement(Aspose.ThreeD.Entities.VertexElement element);

{{< /highlight >}}

I nuovi metodi aggiunti vengono utilizzati per mantenere lo API coerente tra le API Aspose.3D for Java e Aspose.3D for .NET

**Esempio di codice-C#**

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

VertexElement uv = new VertexElementUV();

mesh.AddElement(uv);

{{< /highlight >}}
#### **Rimuove GetControlPointIndex da Aspose.ThreeD.Entities.NurbsSurface class**
**Definizione-C#**

{{< highlight "java" >}}

 public int GetControlPointIndex(int u, int v)

{{< /highlight >}}
#### **Rimuove i metodi Load, Save e ToBitmap da Aspose.ThreeD.Render.ITextureUnit class**
Questi metodi sono stati contrassegnati come obsoleti nella versione 17.8, le sostituzioni equivalenti possono essere trovate nelle interfacce derivate ITexture1D/ITexture2D/ITextureCubemap.

**Definizione-C#**

{{< highlight "java" >}}

 public void Load(Aspose.ThreeD.Render.TextureData bitmap)

public void Save(string path, System.Drawing.Imaging.ImageFormat format)

public void Save(System.Drawing.Bitmap bitmap)

public System.Drawing.Bitmap ToBitmap()

{{< /highlight >}}
