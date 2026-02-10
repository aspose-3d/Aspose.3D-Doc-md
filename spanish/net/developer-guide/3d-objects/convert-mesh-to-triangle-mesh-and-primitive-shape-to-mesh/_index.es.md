---
title: Convertir malla a malla de triángulo y forma primitiva a malla
type: docs
weight: 30
url: /es/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API permite a los desarrolladores convertir cualquier objeto de malla en malla triangular con un diseño de memoria personalizado del vértice. El diseño de memoria personalizado de Vertex se define mediante la clase Struct o dinámicamente por VertexDeclaration en los ejemplos de código.
---
##  **Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API permite a los desarrolladores convertir cualquier objeto de malla a malla triangular con un diseño de memoria personalizado del vértice. El diseño de memoria personalizado de Vertex se define utilizando la clase Struct o dinámicamente por [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) en los ejemplos de código.

{{% alert color="primary" %}}

Este tema de ayuda crea mallas de la caja y la esfera para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear una malla de cubo 3D](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Estos ejemplos muestran cómo:

- [Convertir una malla de esfera a triángulo con diseño de memoria personalizado del vértice (definido en la estructura)](/3d/es/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convertir una malla de caja a triángulo con diseño de memoria personalizado del vértice (definido por la clase VertexDeclaration)](/3d/es/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convertir malla**
Los desarrolladores pueden convertir malla en malla triangular porque cualquier estructura compleja (de superficie) se puede representar como un montón de triángulos. El triángulo es la geometría más atómica. Así se utiliza como base para casi cualquier cosa.
###  **Acceda a los vértices de una malla triangular**
Los desarrolladores pueden acceder a índices, vértices reales, vértices antes de fusionar y total de bytes de vértices en la memoria.

A continuación, el ejemplo convierte una esfera en una malla triangular con un diseño de memoria personalizado.

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




El siguiente ejemplo convierte una malla Box en triángulo con un diseño de memoria personalizado.

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
##  **Convertir la primitiva a una malla**
Usando Aspose.3D for .NET, los desarrolladores pueden convertir cualquier objeto primitivo en una malla. Las primitivas incluyen muchos de los objetos más básicos y usados como caja, esfera, plano, cilindro y toro.

{{% alert color="primary" %}}

Cualquier clase que implemente una interfaz `IMeshConvertible` se puede convertir en malla mientras se exporta a cualquier formato de archivo 3D.

{{% /alert %}}
###  **Convertir una esfera a malla**
Una esfera es un objeto geométrico perfectamente redondo en un espacio tridimensional que aparece en todas partes, desde balones deportivos hasta planetas en el espacio. Usemos la Esfera primitiva para crear una malla.
El ejemplo de código a continuación convierte una esfera en malla.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir una caja a malla**
Una caja describe una variedad de contenedores y receptáculos para uso permanente como almacenamiento, o para uso temporal, a menudo para transportar contenido. Usemos la caja primitiva para crear una malla. El ejemplo de código a continuación convierte un Box en malla.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir un avión a malla**
Un plano se extiende infinitamente sin espesor. Un ejemplo de plano es un plano de coordenadas. Usaremos la primitiva `Plane` para crear una malla. El siguiente ejemplo de código convierte un `Plane` a `Mesh`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir un cilindro a malla**
Un cilindro es una de las formas geométricas curvilíneas más básicas, la superficie formada por los puntos a una distancia fija de una línea recta dada, el eje del cilindro. Se puede utilizar en muchos lugares, por ejemplo, como pilar frente a una casa o como eje de transmisión de automóviles. Permite usar el cilindro primitivo para crear una malla. El ejemplo de código a continuación convierte un cilindro en malla.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir un torus a malla**
Un toro es una superficie de revolución generada al girar un círculo en un espacio tridimensional alrededor de un eje coplanar con el círculo. Si el eje de revolución no toca el círculo, la superficie tiene forma de anillo y se llama toro de revolución. Usemos el primitivo Torus para crear una malla. El siguiente ejemplo de código convierte un Torus a malla.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
