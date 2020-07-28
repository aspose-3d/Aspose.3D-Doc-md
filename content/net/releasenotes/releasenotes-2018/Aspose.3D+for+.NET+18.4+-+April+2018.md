+++
title = "Aspose.3D for .NET 18.4 - April 2018" 
description = "" 
weight = 12122 
+++

Aspose.3D for .NET : Aspose.3D for .NET 18.4 - April 2018  

# Aspose.3D for .NET : Aspose.3D for .NET 18.4 - April 2018


This page contains release notes for [Aspose.3D for .NET 18.4](https://www.nuget.org/packages/Aspose.3D/18.4.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-376|Add skin controller export support in Collada|New Feature|
|THREEDNET-377|Add property animation support in Collada exporting|New Feature|
|THREEDNET-373|Add property animation support in Collada importing|New Feature|
|THREEDNET-375|Add skin controller import support in Collada|New Feature|
|THREEDNET-349|Collada is missing Material ID|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

### API changes

The new features (Collada animation importing and exporting) in 18.4 do not introduce API changes.

The API changes in 18.4 are in two categories:

1.  For the consistence in Aspose.3D for Java API
2.  Removed obsoleted methods

#### SetData and SetIndices methods to Aspose.ThreeD.Entities.VertexElement class

**Definition - C#**

{{< code lang="cs" >}}
/// <summary>
/// Load data
/// </summary>
/// <param name="data"></param>
public void SetData([] data);
/// <summary>
/// Load indices
/// </summary>
/// <param name="data"></param>
public void SetIndices(int[] data);
{{< /code >}}

The new added methods are used to keep the API consistent between Aspose.3D for Java and Aspose.3D for .NET:

**Code example - C#**

{{< code lang="cs" >}}
//Modified from https://github.com/aspose-3d/Aspose.3D-for-.NET/blob/master/Examples/CSharp/Geometry-and-Hierarchy/SetupUVOnCube.cs
// UVs
Vector4[] uvs = new Vector4[]
{
    new Vector4( 0.0, 1.0,0.0, 1.0),
    new Vector4( 1.0, 0.0,0.0, 1.0),
    new Vector4( 0.0, 0.0,0.0, 1.0),
    new Vector4( 1.0, 1.0,0.0, 1.0)
};

// Indices of the uvs per each polygon
int[] uvsId = new int[]
{
    0,1,3,2,2,3,5,4,4,5,7,6,6,7,9,8,1,10,11,3,12,0,2,13
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();

// Create UVset
VertexElementUV elementUV = mesh.CreateElementUV(TextureMapping.Diffuse, MappingMode.PolygonVertex, ReferenceMode.IndexToDirect);
// Copy the data to the UV vertex element 
elementUV.SetData(uvs); //Equivalent to elementUV.Data.AddRange(uvs);
elementUV.SetIndices(uvsId); // Equivalent to elementUV.Indices.AddRange(uvsId);
{{< /code >}}

#### Adds AddChildNode method to Aspose.ThreeD.Node class

**Definition - C#**

{{< code lang="cs" >}}
/// <summary>
/// Add a child node to this node
/// </summary>
/// <param name="node">The child node to be attached</param>
public void AddChildNode(Aspose.ThreeD.Node node);
{{< /code >}}

**Code Example - C#**

{{< code lang="cs" >}}
Scene scene = new Scene();
Node newChild = new Node();
scene.RootNode.AddChildNode(newChild); // Equivalent to scene.RootNode.ChildNodes.Add(newChild);
{{< /code >}}

#### Adds AddElement method to Aspose.ThreeD.Entities.Geometry class

**Definition - C#**

{{< code lang="cs" >}}
/// <summary>
/// Adds an existing vertex element to current geometry
/// </summary>
/// <param name="element">The vertex element to add</param>
public void AddElement(Aspose.ThreeD.Entities.VertexElement element);
{{< /code >}}

The new added methods are used to keep the API consistent between Aspose.3D for Java and Aspose.3D for .NET APIs

**Code example - C#**

{{< code lang="cs" >}}
Mesh mesh = new Mesh();
VertexElement uv = new VertexElementUV();
mesh.AddElement(uv);
{{< /code >}}

#### Removes GetControlPointIndex from Aspose.ThreeD.Entities.NurbsSurface class

**Definition - C#**

public int GetControlPointIndex(int u, int v)

#### Removes Load, Save and ToBitmap methods from Aspose.ThreeD.Render.ITextureUnit class

These methods were marked as obsoleted in version 17.8, the equivalent replacements can be found in the derived interfaces ITexture1D/ITexture2D/ITextureCubemap.

**Definition - C#**

public void Load(Aspose.ThreeD.Render.TextureData bitmap)public void Save(string path, System.Drawing.Imaging.ImageFormat format)public void Save(System.Drawing.Bitmap bitmap)public System.Drawing.Bitmap ToBitmap()

## Attachments:

![](https://docs2.aspose.com/3d/net/images/icons/bullet_blue.gif) [rtorus.png](https://docs2.aspose.com/3d/net/attachments/64455821/64716870.png) (image/png)  

