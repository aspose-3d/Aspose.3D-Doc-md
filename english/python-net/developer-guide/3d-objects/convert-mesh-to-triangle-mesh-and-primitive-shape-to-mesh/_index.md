---
title: Convert Mesh to Triangle Mesh and Primitive Shape to Mesh
type: docs
weight: 30
url: /python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Python via .NET API allows developers to convert any mesh object to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined using the Struct or dynamically by VertexDeclaration class in the code examples.
---

## **Convert a Mesh to Triangle Mesh with Custom Memory Layout of the Vertex**
[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API allows developers to convert any mesh object to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined using the Struct or dynamically by [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration) class in the code examples.

{{% alert color="primary" %}}

This help topic creates meshes from the box and sphere to keep the code comprehensive and short. Developers may construct a mesh manually as narrated in this help topic: [Create a 3D Cube Mesh](/3d/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

These examples show how to:

- [Convert a Sphere to Triangle Mesh with custom memory layout of the vertex (defined in the Struct)](/3d/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert a Box to Triangle Mesh with custom memory layout of the vertex (defined by VertexDeclaration class)](/3d/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Convert Mesh**
Developers may convert mesh to triangle mesh because any complex (surface) structure can be represented as a bunch of triangles. The triangle is the most atomic geometry. Thus it is used as base for almost anything.
### **Access Vertices of a Triangle Mesh**
Developers can access Indices, actual vertices, vertices before merging and total bytes of vertices in memory.

Below example converts a Sphere to triangle mesh with custom memory layout.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




Below example converts a Box to triangle mesh with custom memory layout.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
## **Convert the `Primitive` to a `Mesh`**
Using Aspose.3D for Python via .NET, developers can convert any primitive object to a mesh. Primitives include many of the most basic and most used objects like box, sphere, plane, cylinder, and torus.

{{% alert color="primary" %}}

Any class that implements an interface IMeshConvertible can be converted to mesh while exporting to any 3D file format.

{{% /alert %}}
### **Convert a `Sphere` to `Mesh`**
A sphere is a perfectly round geometrical object in three-dimensional space that appear everywhere from sports balls to planets in space. Let’s use the Sphere primitive to create a mesh.
The code example below converts a Sphere to mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.py" >}}
### **Convert a `Box` to `Mesh`**
A Box describes a variety of containers and receptacles for permanent use as storage, or for temporary use, often for transporting contents. Let’s use the Box primitive to create a mesh. The code example below converts a Box to mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.py" >}}
### **Convert a `Plane` to `Mesh`**
A plane extends infinitely without thickness. An example of a plane is a coordinate plane. Lets use the Plane primitive to create a mesh. The code example below converts a Plane to mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.py" >}}
### **Convert a `Cylinder` to `Mesh`**
A cylinder is one of the most basic curvilinear geometric shapes, the surface formed by the points at a fixed distance from a given straight line, the axis of the cylinder. It can be used in many places, for example as a pillar in front of a home or as a car driveshaft. Lets use the Cylinder primitive to create a mesh. The code example below converts a Cylinder to mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.py" >}}
### **Convert a `Torus` to `Mesh`**
A torus is a surface of revolution generated by revolving a circle in three-dimensional space about an axis coplanar with the circle. If the axis of revolution does not touch the circle, the surface has a ring shape and is called a torus of revolution. Let’s use the Torus primitive to create a mesh. The code example below converts a Torus to mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.py" >}}
