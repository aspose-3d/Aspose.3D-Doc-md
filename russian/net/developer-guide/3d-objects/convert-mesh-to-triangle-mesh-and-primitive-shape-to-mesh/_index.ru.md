---
title: Преобразование сетки в треугольную сетку и примитивной формы в сетку
type: docs
weight: 30
url: /ru/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API позволяет разработчикам преобразовать любой объект сетки в треугольную сетку с пользовательским расположением памяти вершины. Пользовательская компоновка памяти Vertex определяется с помощью Struct или динамически классом VertexDeclaration в примерах кода.
---
##  **Преобразуйте сетку в треугольную сетку с пользовательской компоновкой памяти вертекса**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API позволяет разработчикам преобразовать любой объект сетки в треугольную сетку с пользовательским расположением памяти вершины. Пользовательская компоновка памяти Vertex определяется с помощью Struct или динамически классом [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) в примерах кода.

{{% alert color="primary" %}}

Этот раздел справки создает сетки из коробки и сферы, чтобы код был исчерпывающим и коротким. Разработчики могут создавать сетку вручную, как рассказывают в этой теме справки: [Создайте сетку-куб 3D](/3d/ru/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Эти примеры показывают, как:

- [Преобразование сферы в треугольную сетку с настраиваемой компоновкой памяти вершины (определена в Struct)](/3d/ru/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Преобразуйте коробку в треугольную сетку с пользовательским расположением памяти вершины (определяется классом VertexDeclaration)](/3d/ru/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Конвертируйте сетку**
Разработчики могут преобразовывать сетку в треугольную сетку, потому что любая сложная (поверхностная) структура может быть представлена в виде группы треугольников. Треугольник-самая атомарная геометрия. Таким образом, он используется как база практически для чего угодно.
###  **Вершины доступа треугольной сетки**
Разработчики могут получить доступ к индексам, фактическим вершинам, вершинам до слияния и общему количеству байтов вершин в памяти.

Ниже примера преобразует Sphere в треугольную сетку с пользовательским макетом памяти.

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




Ниже примера преобразует Box в треугольную сетку с пользовательским макетом памяти.

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
##  **Преобразовать примитивный в сетку**
Используя Aspose.3D for .NET, разработчики могут преобразовать любой примитивный объект в сетку. Примитивы включают в себя многие из самых основных и наиболее часто используемых объектов, таких как коробка, сфера, плоскость, цилиндр и тор.

{{% alert color="primary" %}}

Любой класс, реализующий интерфейс `IMeshConvertible`, может быть преобразован в mesh при экспорте в любой формат файла 3D.

{{% /alert %}}
###  **Преобразование сферы в сетку**
Сфера-это идеально круглый геометрический объект в трехмерном пространстве, который появляется повсюду, от спортивных мячей до планет в космосе. Давайте использовать примитив Sphere для создания сетки.
Пример кода ниже преобразует Сферу в сетку.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Конвертировать коробку в сетку**
Коробка описывает различные контейнеры и емкости для постоянного использования в качестве хранилища или для временного использования, часто для транспортировки содержимого. Давайте использовать примитивный ящик для создания сетки. Пример кода ниже преобразует Box в сетку.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Преобразование плоскости в сетку**
Плоскость простирается бесконечно без толщины. Примером плоскости является координатная плоскость. Для создания сетки используется примитив `Plane`. Пример кода ниже преобразует `Plane` в `Mesh`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Преобразование цилиндра в сетку**
Цилиндр-одна из самых основных криволинейных геометрических форм, поверхность, образованная точками на фиксированном расстоянии от заданной прямой линии, оси цилиндра. Его можно использовать во многих местах, например, в качестве стойки перед домом или в качестве приводного вала автомобиля. Для создания сетки позволяет использовать примитивный цилиндр. Пример кода ниже преобразует цилиндр в сетку.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Конвертировать Torus в Mesh**
Тор-это поверхность вращения, порожденная вращением окружности в трехмерном пространстве вокруг оси, копланарной окружности. Если ось вращения не касается круга, поверхность имеет форму кольца и называется тор вращения. Давайте использовать примитив Torus для создания сетки. Пример кода ниже преобразует Torus в сетку.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
