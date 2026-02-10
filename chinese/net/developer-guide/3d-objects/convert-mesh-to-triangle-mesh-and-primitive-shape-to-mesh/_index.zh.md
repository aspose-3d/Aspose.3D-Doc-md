---
title: 将网格转换为三角形网格，将原始形状转换为网格
type: docs
weight: 30
url: /zh/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API 允许开发人员使用顶点的自定义内存布局将任何网格对象转换为三角形网格。在代码示例中，使用Struct或dynamic by VertexDeclaration类定义顶点的自定义内存布局。
---
##  **使用顶点的自定义内存布局将网格转换为三角形网格**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API 允许开发人员使用顶点的自定义内存布局将任何网格对象转换为三角形网格。顶点的自定义内存布局是使用Struct定义的，或者在代码示例中由 [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) 类动态定义。

{{% alert color="primary" %}}

此帮助主题从框和球体创建网格，以保持代码的全面和简短。开发人员可以按照以下帮助主题中的说明手动构建网格: [创建 3D 立方体网格](/3d/zh/net/create-3d-mesh-and-scene/)。

{{% /alert %}}

这些示例显示了如何:

- [使用顶点的自定义内存布局 (在结构中定义) 将球体转换为三角形网格](/3d/zh/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/)。
- [使用顶点的自定义内存布局将框转换为三角形网格 (由VertexDeclaration类定义)](/3d/zh/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/)。
###  **转换网格**
开发人员可能会将网格转换为三角形网格，因为任何复杂 (表面) 结构都可以表示为一堆三角形。三角形是最原子的几何形状。因此，它几乎被用作任何东西的基础。
###  **访问三角形网格的顶点**
开发人员可以访问索引，实际顶点，合并前的顶点以及内存中顶点的总字节。

下面的示例使用自定义内存布局将球体转换为三角形网格。

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




下面的示例使用自定义内存布局将框转换为三角形网格。

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
##  **将图元转换为网格**
使用 Aspose.3D for .NET，开发人员可以将任何基本对象转换为网格。图元包括许多最基本和最常用的对象，如长方体、球体、平面、圆柱体和圆环。

{{% alert color="primary" %}}

在导出为任何 3D 文件格式时，任何实现接口 `IMeshConvertible` 的类都可以转换为网格。

{{% /alert %}}
###  **将球体转换为网格**
球体是三维空间中完美的圆形几何物体，从运动球到太空中的行星无处不在。让我们使用球体原语来创建网格。
下面的代码示例将球体转换为网格。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **将盒子转换为网格**
盒子描述了各种容器和容器，这些容器和容器永久用作存储或临时使用，通常用于运输内容物。让我们使用框原语来创建网格。下面的代码示例将框转换为网格。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **将平面转换为网格**
平面无限延伸而没有厚度。平面的示例是坐标平面。让我们使用 `Plane` 基元创建网格。下面的代码示例将 `Plane` 转换为 `Mesh`。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **将圆柱体转换为网格**
圆柱体是最基本的曲线几何形状之一，由与给定直线 (圆柱体的轴) 相距固定距离的点形成的表面。它可以在许多地方使用，例如作为房屋前面的支柱或汽车驱动轴。让我们使用圆柱原语创建网格。下面的代码示例将圆柱体转换为网格。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **将圆环转换为网格**
圆环是通过在三维空间中绕与圆共面的轴旋转圆而产生的旋转表面。如果旋转轴不接触圆，则表面呈环形，称为圆环。让我们使用圆环原语来创建网格。下面的代码示例将圆环转换为网格。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
