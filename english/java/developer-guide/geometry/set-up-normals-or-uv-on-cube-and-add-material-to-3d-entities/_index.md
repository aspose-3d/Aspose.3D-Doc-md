---
title: Set up normals or UV on Cube and Add Material to 3D Entities
type: docs
weight: 60
url: /java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java offers to manage normals and UV on the geometric shapes. A mesh stores the key properties for every vertex, position in space, and its normal, known as a vector perpendicular to the original surface. The normal is major to shading counts and should be a unit vector. Most mesh formats also support some form of UV coordinates which are a separate 2D representation of the mesh "unfolded" to show what portion of a 2-dimensional texture map to apply to different polygons of the mesh.
---

{{% alert color="primary" %}}

Aspose.3D for Java offers to manage normals and UV on the geometric shapes. A mesh stores the key properties for every vertex, position in space, and its normal, known as a vector perpendicular to the original surface. The normal is major to shading counts and should be a unit vector. Most mesh formats also support some form of UV coordinates which are a separate 2D representation of the mesh "unfolded" to show what portion of a 2-dimensional texture map to apply to different polygons of the mesh.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated here](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by creating a 3D Scene.

{{% /alert %}}
## **Create Normal Vectors**
In order to have a good visual look on lighting, we need to specify normals information for each vertex. In order to have the better details, we can also use normal and diffuse map (use shadow / specular map) to perform per-pixel normal/color. A per-vertex information like normal or vertex color is achieved by VertexElement. In Aspose.3D we can map extra information to control points/polygon vertex/polygon/edge, a sample to define normals for vertex:

{{< highlight "java" >}}
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
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}


The 8 normal vectors are mapped to 8 control points directly, in the next example, we’ll demonstrate a bit more complex scenario.
## **Create UV Coordinates**
Here,we only defined 4 UV coordinates, but applied them to 24 polygon vertices (6 face * 4 vertex per polygon) by using indices.
The Aspose.3D provides 5 mapping modes:

- **ControlPoint** - each data is mapped to the control point of the geometry.
- **PolygonVertex** - the data is mapped to the polygon’s vertex.
- **Polygon** - the data is mapped to the polygon.
- **Edge** - the data is mapped to the edge.
- **AllSame** - one data mapped to the whole geometry.



{{< highlight "java" >}}
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
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Create UVset
VertexElementUV elementUV = mesh.createElementUV(TextureMapping.DIFFUSE, MappingMode.POLYGON_VERTEX, ReferenceMode.INDEX_TO_DIRECT);
// Copy the data to the UV vertex element
elementUV.setData(uvs);
elementUV.setIndices(uvsId);
{{< /highlight >}}
## **Add Materials to 3D Objects**
Aspose.3D for Java allows developers to use shading algorithm for accurate shading and highlights. The Phong has several map inputs which we can use to mask the effect to the node. Physically Based Rendering (PBR) takes some physical properties of objects into account, such an approach provides the appearance of materials as in the real world.
### **Phong Material with Texture for Cube**
When the UV coordinates are ready to use, we can apply a texture on the surface of mesh by using material. Only vertex color cannot describe the details of surface, that’s what materials used for. Here’s an example to attach a Phong material to the cube node:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize cube node object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cubeNode.setEntity(mesh);
// Add cube to the scene
scene.getRootNode().addChildNode(cubeNode);
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
// Initiallize Texture object
Texture diffuse = new Texture();
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Set local file path
diffuse.setFileName(MyDir + "surface.dds");
// Set Texture of the material
mat.setTexture(Material.MAP_DIFFUSE, diffuse);
// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.setFileName("embedded-texture.png");
// Set binary content
diffuse.setContent(Files.readAllBytes(Paths.get(MyDir, "aspose-logo.jpg")));
// Set color
mat.setSpecularColor(new Vector3(1, 0, 0));
// Set brightness
mat.setShininess(100);
// Set material property of the cube object
cubeNode.setMaterial(mat);
MyDir = MyDir + RunExamples.getOutputFilePath("MaterialToCube.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


We specified the diffuse texture mapping, and a specular color with a shininess parameter. 
### **Apply Physically Based Rendering (PBR) Material to a Box**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}
