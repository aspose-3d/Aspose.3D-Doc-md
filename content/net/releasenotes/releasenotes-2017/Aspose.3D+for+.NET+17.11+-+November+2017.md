+++
title = "Aspose.3D for .NET 17.11 - November 2017" 
description = "" 
weight = 12128 
+++

Aspose.3D for .NET : Aspose.3D for .NET 17.11 - November 2017  

# Aspose.3D for .NET : Aspose.3D for .NET 17.11 - November 2017


This page contains release notes for [Aspose.3D for .NET 17.11](https://www.nuget.org/packages/Aspose.3D/17.11.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-303|Add support of importing RVM-binary (AVEVA PDMS)|New feature|
|THREEDNET-305|Add support of merging meshes|New feature|
|THREEDNET-306|FBX to GLTF - incorrect material opacity in GLTF|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Adds RvmText and RvmBinary members to Aspose.ThreeD.FileFormat class

**C#**

{{< code lang="c#" >}}
/// <summary>
/// AVEVA Plant Design Management System Model in text format
/// </summary>
public static readonly FileFormat RvmText;
/// <summary>
/// AVEVA Plant Design Management System Model in binary format
/// </summary>
public static readonly FileFormat RvmBinary;
{{< /code >}}

Auto format detection is supported for PDMS RVM file, so developers can import it directly with the constructor of Scene class without explicitly specifying the FileFormat.

**C#**

Scene scene = new Scene("stablizer.rvm");

The primitives in RVM files will be converted to meshes during the import.

#### Adds Aspose.ThreeD.Formats.RvmLoadOptions class

The properties CylinderRadialSegments, DishLongitudeSegments, DishLatitudeSegments and TorusTubularSegments are used to control the way of converting the primitives defined in Rvm files into meshes. Details can be found in classes Aspose.ThreeD.Entities.Cylinder and Aspose.ThreeD.Entities.Torus

**C#**

/// <summary>/// Load options for AVEVA Plant Design Management System's RVM file./// </summary>public class RvmLoadOptions : LoadOptions{    /// <summary>    /// The RVM file contains no material information, but the Aspose.3D can generate materials for each objects.    /// Default value is true    /// </summary>    public bool GenerateMaterials { get; set; }    /// <summary>    /// Gets or sets the number of cylinder's radial segments, default value is 16    /// </summary>    public int CylinderRadialSegments { get; set; }    /// <summary>    /// Gets or sets the number of dish's longitude segments, default value is 12    /// </summary>    public int DishLongitudeSegments { get; set; }    /// <summary>    /// Gets or sets the number of dish's latitude segments, default value is 8     /// </summary>    public int DishLatitudeSegments { get; set; }    /// <summary>    /// Gets or sets the number of torus's tubular segments, default value is 20     /// </summary>    public int TorusTubularSegments { get; set; }    /// <summary>    /// Construct a <see cref="RvmLoadOptions"/> instance    /// </summary>    /// <param name="contentType"></param>    public RvmLoadOptions(FileContentType contentType);    /// <summary>    /// Construct a <see cref="RvmLoadOptions"/> instance    /// </summary>    public RvmLoadOptions();}

**Sample code:**

**C#**

Scene scene = new Scene();var opt = new RvmLoadOptions(){    CylinderRadialSegments = 32,    DishLatitudeSegments = 16,    DishLongitudeSegments = 24,    TorusTubularSegments = 40};scene.Open("LAD-TOP.rvm", opt);scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

#### 3 members are added into Aspose.ThreeD.Entities.PolygonModifier class

**C#**

/// <summary>/// Convert a whole node to a single transformed mesh/// Vertex elements like normal/texture coordinates are not supported yet/// </summary>/// <param name="node">The node to merge</param>/// <returns>Merged mesh</returns>public static Mesh MergeMesh(Node node)/// <summary>/// Convert a whole scene to a single transformed mesh/// Vertex elements like normal/texture coordinates are not supported yet/// </summary>/// <param name="scene">The scene to merge</param>/// <returns>The merged mesh</returns>public static Mesh MergeMesh(Scene scene);/// <summary>/// Convert a whole node to a single transformed mesh/// Vertex elements like normal/texture coordinates are not supported yet/// </summary>/// <param name="nodes">The nodes to merge</param>/// <returns>Merged mesh</returns>public static Mesh MergeMesh(IList<Node> nodes);

**Sample code:**

**C#**

Scene scene = new Scene("LAD-TOP.rvm");Mesh mesh = PolygonModifier.MergeMesh(scene);FileFormat.PLY.EncodeMesh(mesh, "LAD-TOP.ply");

####   
Transparency member is added to Aspose.ThreeD.Shading.PbrMaterial class

Only GLTF 2.0 supports PBR material, so this improvement only affects the GLTF 2.0 export.

**C#**

/// <summary>///  Gets or sets the transparency factor./// The factor should be ranged between 0(0%, fully opaque) and 1(100%, fully transparent)/// Any invalid factor value will be clampped./// </summary>/// <value>The transparency factor.</value>public double Transparency { get; set; }

**Sample code:**

**C#**

Scene scene = new Scene();scene.RootNode.CreateChildNode("box", new Box()).Material = new PbrMaterial() {Transparency = 0.5, Albedo = new Vector3(Color.AliceBlue)};scene.Save("box.gltf", FileFormat.GLTF2);

#### Usage Examples

Please check the list of help topics added or updated in the Aspose.3D Wiki docs:

1.  [Merge Meshes in 3D file](https://docs2.aspose.com/3d/net/developerguide/3dobjects/merge+meshes+in+3d+file)
2.  [Use RVM load options](https://docs2.aspose.com/3d/net/developerguide/creatingloadingandsaving3dscene/specify+3d+file+load+options#specify3dfileloadoptions-uservmloadoptions)

