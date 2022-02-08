---
title: Set up normals or UV on Cube and Add Material to 3D Entities
type: docs
weight: 60
url: /java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
---

{{% alert color="primary" %}}

Aspose.3D for Java offers to manage normals and UV on the geometric shapes. A mesh stores the key properties for every vertex, position in space, and its normal, known as a vector perpendicular to the original surface. The normal is major to shading counts and should be a unit vector. Most mesh formats also support some form of UV coordinates which are a separate 2D representation of the mesh "unfolded" to show what portion of a 2-dimensional texture map to apply to different polygons of the mesh.

{{% /alert %}} {{% alert color="primary" %}}

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated here](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by creating a 3D Scene.

{{% /alert %}}
## **Create Normal Vectors**
In order to have a good visual look on lighting, we need to specify normals information for each vertex. In order to have the better details, we can also use normal and diffuse map (use shadow / specular map) to perform per-pixel normal/color. A per-vertex information like normal or vertex color is achieved by VertexElement. In Aspose.3D we can map extra information to control points/polygon vertex/polygon/edge, a sample to define normals for vertex:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


The 8 normal vectors are mapped to 8 control points directly, in the next example, we’ll demonstrate a bit more complex scenario.
## **Create UV Coordinates**
Here,we only defined 4 UV coordinates, but applied them to 24 polygon vertices (6 face * 4 vertex per polygon) by using indices.
The Aspose.3D provides 5 mapping modes:

- **ControlPoint** - each data is mapped to the control point of the geometry.
- **PolygonVertex** - the data is mapped to the polygon’s vertex.
- **Polygon** - the data is mapped to the polygon.
- **Edge** - the data is mapped to the edge.
- **AllSame** - one data mapped to the whole geometry.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
## **Add Materials to 3D Objects**
Aspose.3D for Java allows developers to use shading algorithm for accurate shading and highlights. The Phong has several map inputs which we can use to mask the effect to the node. Physically Based Rendering (PBR) takes some physical properties of objects into account, such an approach provides the appearance of materials as in the real world.
### **Phong Material with Texture for Cube**
When the UV coordinates are ready to use, we can apply a texture on the surface of mesh by using material. Only vertex color cannot describe the details of surface, that’s what materials used for. Here’s an example to attach a Phong material to the cube node:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


We specified the diffuse texture mapping, and a specular color with a shininess parameter. 
### **Apply Physically Based Rendering (PBR) Material to a Box**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
