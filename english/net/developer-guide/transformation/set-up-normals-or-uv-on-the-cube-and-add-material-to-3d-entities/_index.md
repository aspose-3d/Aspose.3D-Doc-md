---
title: Set up normals or UV on the Cube and Add Material to 3D Entities
type: docs
weight: 20
url: /net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: How to create normals or uv data on a mesh in Aspose.3D.
---

{{% alert color="primary" %}}

Aspose.3D for .NET offers to manage normals and UV on the geometric shapes. A mesh stores the key properties for every vertex are its position in space and its normal, a vector perpendicular to the original surface. The normal is major to shading counts. The normals should be unit vectors. Most mesh formats also support some form of UV coordinates which are a separate 2d representation of the mesh "unfolded" to show what portion of a 2-dimensional texture map to apply to different polygons of the mesh.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by [Creating a 3D Scene](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Create Normal Vectors**
To have a good visual look on lighting, we need to specify normals information for each vertex, to have a better details, we can also use normal and diffuse map (sure you can use shadow / specular map) to perform per-pixel normal/color. A per-vertex information like normal or vertex color is achieved by VertexElement. In Aspose.3D we can map extra information to control points/polygon vertex/polygon/edge, a sample to define normals for vertex:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;
// Copy the data to the vertex element
elementNormal.Data.AddRange(normals);

{{< /highlight >}}

The 8 normal vectors are mapped to 8 control points directly, in the next example, we’ll demonstrate a bit more complex scenario.
## **Create UV Coordinates**
Here,we only defined 4 UV coordinates, but applied them to 24 polygon vertices (6 face * 4 vertex per polygon) by using indices.
The Aspose.3D provides 5 mapping modes:

- `ControlPoint` - each data is mapped to the control point of the geometry.
- `PolygonVertex` - the data is mapped to the polygon’s vertex.
- `Polygon` - the data is mapped to the polygon.
- `Edge` - the data is mapped to the edge.
- `AllSame` - one data mapped to the whole geometry.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
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
elementUV.Data.AddRange(uvs);
elementUV.Indices.AddRange(uvsId);

{{< /highlight >}}
## **Add Materials to 3D Objects**
Aspose.3D for .NET allows developers to use shading algorithm for accurate shading and highlights. The Phong has several map inputs which we can use to mask the effect to the node. Physically Based Rendering (PBR) takes some physical properties of objects into account, such an approach provides the appearance of materials as in the real world.
### **Phong Material with Texture for Cube**
When the UV coordinates are ready to use, we can apply a texture on the surface of mesh by using material. Only vertex color cannot describe the details of surface, that’s what materials used for. Here’s an example to attach a Phong material to the cube node:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
            
// Initialize cube node object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
         
// Point node to the mesh
cubeNode.Entity = mesh;
            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);
            
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
            
// Initiallize Texture object
Texture diffuse = new Texture();
            
// The path to the documents directory.
            
// Set local file path
diffuse.FileName = RunExamples.GetOutputFilePath("surface.dds");

// Set Texture of the material
mat.SetTexture("DiffuseColor", diffuse);

// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.FileName = "embedded-texture.png";
// Set binary content
diffuse.Content = File.ReadAllBytes(RunExamples.GetDataFilePath("aspose-logo.jpg"));

// Set color
mat.SpecularColor = new Vector3(Color.Red);

// Set brightness
mat.Shininess = 100;

// Set material property of the cube object
cubeNode.Material = mat;
            
// Save 3D scene in the supported file formats
scene.Save("MaterialToCube.fbx");

{{< /highlight >}}

We specified the diffuse texture mapping, and a specular color with a shininess parameter. 
### **Apply Physically Based Rendering (PBR) Material to a Box**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

**.NET, C#**

{{< highlight java >}}

 // initialize a scene

Scene scene = new Scene();

// initialize PBR material object

PbrMaterial mat = new PbrMaterial();

// an almost metal material

mat.MetallicFactor = 0.9;

// material surface is very rough

mat.RoughnessFactor = 0.9;

// create a box to which the material will be applied

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

// save 3d scene into STL format

scene.Save(@"C:\3D\PBR_Material_Box_Out.stl", FileFormat.STLASCII);

{{< /highlight >}}
