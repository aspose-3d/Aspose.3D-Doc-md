---
title: Public API Changes in Aspose.3D 1.5.0
type: docs
weight: 20
url: /net/public-api-changes-in-aspose-3d-1-5-0/
---

**Contents Summary**

- [Convert the Primitive to a Mesh and Create a Scene from Primitive 3D Models](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convert a Mesh to Triangle Mesh with Custom Memory Layout of the Vertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Split Mesh](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Removal of Distreet3DS format.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Adds Discreet3DS format.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.4.0 to 1.5.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **Convert the Primitive to a Mesh and Create a Scene from Primitive 3D Models**
**Various Classes, Methods and Properties are added**

- **Adds interface Aspose.ThreeD.Entities.IMeshConvertible.** 
  - Any class that implements this interface can be converted to mesh while exporting to any 3D file formats.
- **Adds class Aspose.ThreeD.Entities.Primitive.** 
  - It is derived from Entity class and also the base class for all primitive classes.
- **Adds class Aspose.ThreeD.Entities.Box/Cylinder/Plane/Sphere/Torus.** 
  - These can be used to define scene with simple primitives. Developers can also convert them to mesh automatically.

Primitives include many of the most basic and most used objects like box, sphere, plane, cylinder, and torus. Developers may also convert them to mesh for the modification purposes. These help topics illustrate how to do so: [Convert the Primitive to a Mesh](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) and [Convert the Primitive to a Mesh](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Convert a Mesh to Triangle Mesh with Custom Memory Layout of the Vertex**
**Various Classes, Methods and Properties are added**

- **Adds class Aspose.ThreeD.Entities.TriMesh/TriMesh<T>** 
  - TriMesh/TriMesh<T> contains the definition for triangle-based meshes with custom memory layout, which is useful when developer requires to convert the scene to their own proprietary file formats or in rendering.
- **Adds structure Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4** 
  - These classes present vector components in the float. Only a few modern GPU supports double-precision vector, single-precision float types are more welcomed in real-time rendering world. These replacements will co-exist with the original Vector2/Vector3/Vector4 since they play different roles in Aspose.3D. Double-precision is mainly used to store model’s data because it has less accumulated error. Single-precision is mainly used in rendering or user’s own proprietary file formats conversion because it has better acceptance and performance. We introduced this set of vectors in Aspose.3D 1.5 because we added support for custom vertex layout, where the float vectors will be frequently used.
- **Adds attribute class Aspose.ThreeD.Utilities.SemanticAttribute** 
  - Developer can define custom structure for vertex, and use this attribute to mark the semantic of the fields.
- **Adds class Aspose.ThreeD.Utilities.VertexDeclaration** 
  - It describes the memory layout of the vertex.
- **Adds enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic** 
  - These enum types annotate the vertex’s field’s data type and semantic respectively.
- **Adds class Aspose.ThreeD.Utilities.VertexField** 
  - It describes each field in the custom memory layout of Vertex.
- **Adds class Aspose.ThreeD.Utilities.Vertex** 
  - It can be used to access the raw vertex in TriMesh/TriMesh<T>

Developers may convert any mesh object to the triangle mesh with the custom memory layout of the vertex. The graphic software packages and hardware devices operate more efficiently on triangles. This help topic illustrates how to do so: [Convert a Mesh to Triangle Mesh with Custom Memory Layout of the Vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Split Mesh**
**Various Classes, Methods and Properties are added**

- **Adds enum Aspose.ThreeD.Entities.SplitMeshPolicy** 
  - It specifies the data policy used in the mesh splitting algorithm, we support two policies, share data between sub-meshes or each sub-mesh has its own data (Only used data).
- **Adds 3 SplitMesh methods to Aspose.ThreeD.Entities.PolygonModifier class** 
  1. Split meshes on a specified node to sub-meshes by material definition.
  1. Split all mesh in the given scene to sub-meshes by material definition.
  1. Split the given mesh to sub-meshes by material definition.
- **Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig** 
  - It allows users to flip the coordinate system of U3D during import or export.

Developers may require to automatically split a mesh by material, so that each mesh is only using one material or split mesh by specifying the material. These help topics illustrate how to do so: [Split a Mesh by Specifying the Material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) and [Split All Meshes of a Scene Per Material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Removal of Distreet3DS format.**
Distreet3DS format is marked as obsolete due to the incorrect spell.
### **Adds Discreet3DS format.**
Discreet3DS format has been introduced.
### **Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig**
It allows users to flip the coordinate system of U3D during import or export.
