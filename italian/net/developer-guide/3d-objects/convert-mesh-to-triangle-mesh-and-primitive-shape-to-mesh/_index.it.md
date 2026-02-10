---
title: Convertire mesh in mesh triangolare e forma primitiva in mesh
type: docs
weight: 30
url: /it/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API consente agli sviluppatori di convertire qualsiasi oggetto mesh in mesh triangolare con layout di memoria personalizzato del vertice. Il layout di memoria personalizzato di Vertex viene definito utilizzando Struct o dinamicamente dalla classe VertexDeclaration negli esempi di codice.
---
##  **Convertire una mesh in mesh triangolare con layout di memoria personalizzato del vertice**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API consente agli sviluppatori di convertire qualsiasi oggetto mesh in mesh triangolare con layout di memoria personalizzato del vertice. Il layout di memoria personalizzato di Vertex viene definito utilizzando Struct o dinamicamente dalla classe [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) negli esempi di codice.

{{% alert color="primary" %}}

Questo argomento di aiuto crea mesh dalla casella e dalla sfera per mantenere il codice completo e breve. Gli sviluppatori possono costruire una mesh manualmente come narrato in questo argomento di aiuto: [Crea una mesh cubica da 3D](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Questi esempi mostrano come:

- [Convert a Sphere to Triangle Mesh with custom memory layout of the vertex (defined in the Struct)](/3d/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert a Box to Triangle Mesh with custom memory layout of the vertex (defined by VertexDeclaration class)](/3d/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convertire Mesh**
Gli sviluppatori possono convertire la mesh in una mesh triangolare perché qualsiasi struttura complessa (di superficie) può essere rappresentata come un gruppo di triangoli. Il triangolo è la geometria più atomica. Quindi è usato come base per quasi tutto.
###  **Vertici di accesso di una mesh triangolare**
Gli sviluppatori possono accedere a indici, vertici effettivi, vertici prima della fusione e byte totali dei vertici in memoria.

Il seguente esempio converte una mesh Sfera in triangolo con il layout di memoria personalizzato.

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




Il seguente esempio converte una mesh box in triangolare con layout di memoria personalizzato.

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
##  **Convertire il primitivo in una maglia**
Utilizzando Aspose.3D for .NET, gli sviluppatori possono convertire qualsiasi oggetto primitivo in una mesh. I primitivi includono molti degli oggetti più elementari e più utilizzati come scatola, sfera, piano, cilindro e toro.

{{% alert color="primary" %}}

Qualsiasi classe che implementa un'interfaccia `IMeshConvertible` può essere convertita in mesh durante l'esportazione in qualsiasi formato di file 3D.

{{% /alert %}}
###  **Convertire una sfera in mesh**
Una sfera è un oggetto geometrico perfettamente rotondo nello spazio tridimensionale che appare ovunque, dalle palle sportive ai pianeti nello spazio. Usiamo la Sfera primitiva per creare una mesh.
L'esempio di codice seguente converte una sfera in mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertire una scatola in mesh**
Una scatola descrive una varietà di contenitori e recipienti per uso permanente come deposito o per uso temporaneo, spesso per il trasporto di contenuti. Usiamo la scatola primitiva per creare una mesh. L'esempio di codice seguente converte un Box in mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertire un aereo in rete**
Un piano si estende all'infinito senza spessore. Un esempio di un aereo è un piano di coordinate. Consente di utilizzare la primitiva `Plane` per creare una mesh. L'esempio di codice di seguito converte da `Plane` a `Mesh`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertire un cilindro in rete**
Un cilindro è una delle forme geometriche curvilinee più elementari, la superficie formata dai punti a distanza fissa da una data linea retta, l'asse del cilindro. Può essere utilizzato in molti luoghi, ad esempio come pilastro davanti a una casa o come albero motore per auto. Consente di utilizzare il cilindro primitivo per creare una mesh. L'esempio di codice seguente converte un cilindro in mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertire un Torus in Mesh**
Un toro è una superficie di rivoluzione generata ruotando un cerchio nello spazio tridimensionale attorno a un asse complanare con il cerchio. Se l'asse di rivoluzione non tocca il cerchio, la superficie ha una forma ad anello ed è chiamata toro di rivoluzione. Usiamo il Torus primitivo per creare una mesh. L'esempio di codice seguente converte un Torus in mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
