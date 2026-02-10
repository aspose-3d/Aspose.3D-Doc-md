---
title: Convert Mesh to Triangle Mesh and Primitive Shape to Mesh
type: docs
weight: 30
url: /net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API allows developers to convert any mesh object to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined using the Struct or dynamically by VertexDeclaration class in the code examples.
---

## **Convert a Mesh to Triangle Mesh with Custom Memory Layout of the Vertex**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API allows developers to convert any mesh object to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined using the Struct or dynamically by [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) class in the code examples.

{{% alert color="primary" %}}

This help topic creates meshes from the box and sphere to keep the code comprehensive and short. Developers may construct a mesh manually as narrated in this help topic: [Create a 3D Cube Mesh](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}

These examples show how to:

- [Convert a Sphere to Triangle Mesh with custom memory layout of the vertex (defined in the Struct)](/3d/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert a Box to Triangle Mesh with custom memory layout of the vertex (defined by VertexDeclaration class)](/3d/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Convert Mesh**
Developers may convert mesh to triangle mesh because any complex (surface) structure can be represented as a bunch of triangles. The triangle is the most atomic geometry. Thus it is used as base for almost anything.
### **Access Vertices of a Triangle Mesh**
Developers can access Indices, actual vertices, vertices before merging and total bytes of vertices in memory.

Below example converts a Sphere to triangle mesh with custom memory layout.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
[StructLayout(LayoutKind.Sequential)]
struct MyVertex
{
    [Semantic(VertexFieldSemantic.Position)]
    FVector3 position;
    [Semantic(VertexFieldSemantic.Normal)]
    FVector3 normal;
}

public static void Run()
{
    // Initialize scene object
    Scene scene = new Scene();

    // Initialize Node class object
    Node cubeNode = new Node("sphere");

    Mesh sphere = (new Sphere()).ToMesh();
    // Convert any mesh into typed TriMesh
    var myMesh = TriMesh<MyVertex>.FromMesh(sphere);
    // Get the vertex data in customized vertex structure.
    MyVertex[] vertex = myMesh.VerticesToTypedArray();
    // Get the 32bit and 16bit indices
    int[] indices32bit;
    ushort[] indices16bit;
    myMesh.IndicesToArray(out indices32bit);
    myMesh.IndicesToArray(out indices16bit);
    using (MemoryStream ms = new MemoryStream())
    {
        // Or we can write the vertex directly into stream like:
        myMesh.WriteVerticesTo(ms);
        // The indice data can be directly write to stream, we support 32-bit and 16-bit indice.
        myMesh.Write16bIndicesTo(ms);
        myMesh.Write32bIndicesTo(ms);
    }
    // Point node to the Mesh geometry
    cubeNode.Entity = sphere;

    // Add Node to a scene
    scene.RootNode.ChildNodes.Add(cubeNode);

    // The path to the documents directory.
    string output = RunExamples.GetOutputFilePath("SphereToTriangleMeshCustomMemoryLayoutScene.fbx");

    // Save 3D scene in the supported file formats
    scene.Save(output, FileFormat.FBX7400ASCII);

    Console.WriteLine("Indices = {0}, Actual vertices = {1}, vertices before merging = {2}", myMesh.IndicesCount, myMesh.VerticesCount, myMesh.UnmergedVerticesCount);
    Console.WriteLine("Total bytes of vertices in memory {0}bytes", myMesh.VerticesSizeInBytes);
    Console.WriteLine("\n Converted a Sphere mesh to triangle mesh with custom memory layout of the vertex successfully.\nFile saved at " + output);
}

{{< /highlight >}}




Below example converts a Box to triangle mesh with custom memory layout.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Get mesh of the Box
Mesh box = (new Box()).ToMesh();
// Create a customized vertex layout
VertexDeclaration vd = new VertexDeclaration();
VertexField position = vd.AddField(VertexFieldDataType.FVector4, VertexFieldSemantic.Position);
vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Normal);
// Get a triangle mesh
TriMesh triMesh = TriMesh.FromMesh(box);

{{< /highlight >}}
## **Convert the Primitive to a Mesh**
Using Aspose.3D for .NET, developers can convert any primitive object to a mesh. Primitives include many of the most basic and most used objects like box, sphere, plane, cylinder, and torus.

{{% alert color="primary" %}}

Any class that implements an interface `IMeshConvertible` can be converted to mesh while exporting to any 3D file format.

{{% /alert %}}
### **Convert a Sphere to Mesh**
A sphere is a perfectly round geometrical object in three-dimensional space that appear everywhere from sports balls to planets in space. Let’s use the Sphere primitive to create a mesh.
The code example below converts a Sphere to mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
### **Convert a Box to Mesh**
A Box describes a variety of containers and receptacles for permanent use as storage, or for temporary use, often for transporting contents. Let’s use the Box primitive to create a mesh. The code example below converts a Box to mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
### **Convert a Plane to Mesh**
A plane extends infinitely without thickness. An example of a plane is a coordinate plane. Lets use the `Plane` primitive to create a mesh. The code example below converts a `Plane` to `Mesh`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
### **Convert a Cylinder to Mesh**
A cylinder is one of the most basic curvilinear geometric shapes, the surface formed by the points at a fixed distance from a given straight line, the axis of the cylinder. It can be used in many places, for example as a pillar in front of a home or as a car driveshaft. Lets use the Cylinder primitive to create a mesh. The code example below converts a Cylinder to mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
### **Convert a Torus to Mesh**
A torus is a surface of revolution generated by revolving a circle in three-dimensional space about an axis coplanar with the circle. If the axis of revolution does not touch the circle, the surface has a ring shape and is called a torus of revolution. Let’s use the Torus primitive to create a mesh. The code example below converts a Torus to mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
