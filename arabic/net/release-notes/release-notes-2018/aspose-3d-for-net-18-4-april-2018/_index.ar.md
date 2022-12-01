---
title: Aspose.3D for .NET 18.4-pripril 2018
type: docs
weight: 90
url: /ar/net/aspose-3d-for-net-18-4-april-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 18.4](https://www.nuget.org/packages/Aspose.3D/18.4.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-376|Add الجلد تحكم دعم التصدير في Collada|New eature|
|THREEDNET-377|Add دعم الرسوم المتحركة الملكية في Collada التصدير|New eature|
|THREEDNET-373|Add دعم الرسوم المتحركة الملكية في Collada الاستيراد|New eature|
|THREEDNET-375|Add الجلد تحكم استيراد الدعم في Collada|New eature|
|THREEDNET-349|Collada مفقود Material aterD|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
### **API التغييرات**
The الميزات الجديدة (Collada الرسوم المتحركة استيراد وتصدير) في 18.4 لا تقدم API التغييرات.

The API التغييرات في 18.4 هي في فئتين:

1. Fأو الاتساق في Aspose.3D for Java API
1. Rطرق تعبيري obsoleted
#### **SetData و etetIndking طرق إلى Aspose.ThreeD. nntities. Vertexlement الفئة**
**Defintion-C#**

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

Tتم استخدام طرق جديدة إضافية للحفاظ على API متسقة بين Aspose.3D for Java و Aspose.3D for .NET:

**Oقصيدة مثال-C#**

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
#### **Adds AddChildNطريقة ode إلى Aspose.ThreeD.**
**Defintion-C#**

{{< highlight "java" >}}

 /// <summary>

/// Add a child node to this node

/// </summary>

/// <param name="node">The child node to be attached</param>

public void AddChildNode(Aspose.ThreeD.Node node);

{{< /highlight >}}

**Code Example - C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

Node newChild = new Node();

scene.RootNode.AddChildNode(newChild); // Equivalent to scene.RootNode.ChildNodes.Add(newChild);

{{< /highlight >}}


#### **Adds Aطريقة ddElement إلى Aspose.ThreeD. nntities. Gفئة eometry**
**Defintion-C#**

{{< highlight "java" >}}

 /// <summary>

/// Adds an existing vertex element to current geometry

/// </summary>

/// <param name="element">The vertex element to add</param>

public void AddElement(Aspose.ThreeD.Entities.VertexElement element);

{{< /highlight >}}

Tتم استخدام طرق جديدة إضافية للحفاظ على API متسقة بين Aspose.3D for Java و Aspose.3D for .NET AIs

**Oقصيدة مثال-C#**

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

VertexElement uv = new VertexElementUV();

mesh.AddElement(uv);

{{< /highlight >}}
#### **Removes etetControPointIndex من Aspose.ThreeD. nntities. ururbsSurface الفئة**
**Defintion-C#**

{{< highlight "java" >}}

 public int GetControlPointIndex(int u, int v)

{{< /highlight >}}
#### **Removes Load ، Save و methods oBطرق itmap من Aspose.ThreeD.**
تم وضع علامة على أساليب hese كما obsoleted في الإصدار 17.8 ، ويمكن العثور على بدائل مماثلة في واجهات مشتقة Iexture1D/Iexexture2D/exexextureCubemap.

**Defintion-C#**

{{< highlight "java" >}}

 public void Load(Aspose.ThreeD.Render.TextureData bitmap)

public void Save(string path, System.Drawing.Imaging.ImageFormat format)

public void Save(System.Drawing.Bitmap bitmap)

public System.Drawing.Bitmap ToBitmap()

{{< /highlight >}}
