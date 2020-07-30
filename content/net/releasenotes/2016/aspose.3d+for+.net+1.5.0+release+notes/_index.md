---
title : "Aspose.3D for .NET 1.5.0 Release Notes" 
description : "" 
weight : 12147 
toc : false
type: docs
url: /net/releasenotes/2016/aspose.3d+for+.net+1.5.0+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 1.5.0 Release Notes


## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-146|Convert geometries to per-vertex structure.|New Feature|
|THREEDNET-148|Allow user to split mesh per materials.|New Feature|
|THREEDNET-150|Create mesh for plane.|New Feature|
|THREEDNET-151|Create mesh for Box.|New Feature|
|THREEDNET-152|Create mesh for Sphere.|New Feature|
|THREEDNET-153|Create mesh for cylinder.|New Feature|
|THREEDNET-155|Create mesh for torus.|New Feature|
|THREEDNET-145|Allow flip coordinate system in U3D's load/save configuration class.|Enhancement|
|THREEDNET-154|Spell issue: Distreet3DS should be Discreet3DS.|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Removal of Distreet3DS format.

Distreet3DS format is marked as obsolete due to the incorrect spell.

#### Adds Discreet3DS format.

Discreet3DS format has been introduced.

#### Adds interface Aspose.ThreeD.Entities.IMeshConvertible.

Any class that implements this interface can be converted to mesh while exporting to any 3D file formats.

#### Adds class Aspose.ThreeD.Entities.Primitive.

It is derived from Entity class and also the base class for all primitive classes.

#### Adds class Aspose.ThreeD.Entities.Box/Cylinder/Plane/Sphere/Torus

These can be used to define scene with simple primitives. Developers can also convert them to mesh automatically.

#### Adds class Aspose.ThreeD.Entities.TriMesh/TriMesh<T>

TriMesh/TriMesh<T> contains the definition for triangle-based meshes with custom memory layout, which is useful when developer requires to convert the scene to their own proprietary file formats or in rendering.

#### Adds structure Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4

These classes present vector components in the float. Only a few modern GPU supports double-precision vector, single-precision float types are more welcomed in real-time rendering world. These replacements will co-exist with the original Vector2/Vector3/Vector4 since they play different roles in Aspose.3D. Double-precision is mainly used to store model’s data because it has less accumulated error. Single-precision is mainly used in rendering or user’s own proprietary file formats conversion because it has better acceptance and performance. We introduced this set of vectors in Aspose.3D 1.5 because we added support for custom vertex layout, where the float vectors will be frequently used.

#### Adds attribute class Aspose.ThreeD.Utilities.SemanticAttribute

Developer can define custom structure for vertex, and use this attribute to mark the semantic of the fields.

#### Adds class Aspose.ThreeD.Utilities.VertexDeclaration

It describes the memory layout of the vertex.

#### Adds enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic

These enum types annotate the vertex’s field’s data type and semantic respectively.

#### Adds class Aspose.ThreeD.Utilities.VertexField

It describes each field in the custom memory layout of Vertex.

#### Adds class Aspose.ThreeD.Utilities.Vertex

It can be used to access the raw vertex in TriMesh/TriMesh<T>

#### Adds enum Aspose.ThreeD.Entities.SplitMeshPolicy

It specifies the data policy used in the mesh splitting algorithm, we support two policies, share data between sub-meshes or each sub-mesh has its own data (Only used data).

#### Adds 3 SplitMesh methods to Aspose.ThreeD.Entities.PolygonModifier class

1.  Split meshes on a specified node to sub-meshes by material definition.
2.  Split all mesh in the given scene to sub-meshes by material definition.
3.  Split the given mesh to sub-meshes by material definition.

#### Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig

It allows users to flip the coordinate system of U3D during import or export.

### Usage Examples

Please check the list of help topics added in the Aspose.3D Wiki docs:

*   [Convert the Primitive to a Mesh](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
*   [Create a Scene from Primitive 3D Models](https://docs2.aspose.com/3d/net/developerguide/3dmodeling/create+scene+with+primitive+3d+shapes)
*   [Split a Mesh by Specifying the Material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)
*   [Split All Meshes of a Scene Per Material](https://docs2.aspose.com/3d/net/developerguide/3dobjects/split+mesh)
*   [Convert a Mesh to Triangle Mesh with Custom Memory Layout of the Vertex](https://docs2.aspose.com/3d/net/developerguide/3dobjects/convert+mesh+to+triangle+mesh+and+primitive+shape+to+mesh)

