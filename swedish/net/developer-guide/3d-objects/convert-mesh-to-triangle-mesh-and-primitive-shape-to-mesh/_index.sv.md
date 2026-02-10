---
title: Konvertera Mesh till triangel Mesh och Primitive Form till mesh
type: docs
weight: 30
url: /sv/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API allows developers to convert any mesh object to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined using the Struct or dynamically by VertexDeclaration class in the code examples.
---
##  **Konvertera en mesh till triangeln mesh med egna minneslayout för vertex**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API tillåter utvecklare att konvertera vilket mesh-objekt som helst till triangel mesh med egen layout av vertex. Den egna minneslayouten för Vertex definieras med Struct eller dynamiskt av klassen [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) i kodexempel s.

{{% alert color="primary" %}}

Detta hjälpämne skapar meshes från lådan och sfären för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt som är berättad i detta hjälpämne: [Skapa en 3D kubst](/3d/sv/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Dessa exempel visar hur:

- [Konvertera en sfär till triangeln Mesh med anpassad layout av vertex (definierad i Struct)](/3d/sv/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Konvertera en ruta till triangeln Mesh med egen layout av vertex (definierad av VertexDeclaration klass)](/3d/sv/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Konvertera mask**
Utvecklare kan konvertera mesh till triangeln mesh eftersom alla komplexa (yta) strukturer kan representeras som ett gäng trianglar. Triangeln är den mest atomiska geometrin. Således används den som bas för nästan allt.
###  **Åtkomst hörn av en triangel Mesh**
Utvecklare kan komma åt index, faktiska hörn, hörn före sammanslagning och total byte av hörn i minnet.

Nedan konverterar exempel en Sfär till triangeln mesh med anpassad minne layout.

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




Nedan konverterar exempel en Box till triangel mesh med anpassad minnes layout.

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
##  **Omvandla det primitiva till ett tåg**
Med Aspose.3D for .NET kan utvecklare konvertera vilket primitivt objekt till ett mesh. Primitiv omfattar många av de mest grundläggande och mest använda föremål som låda, sfär, plan, cylinder och torus.

{{% alert color="primary" %}}

Any class that implements an interface `IMeshConvertible` can be converted to mesh while exporting to any 3D file format.

{{% /alert %}}
###  **Konvertera en sfär till mesh**
En sfär är ett perfekt rundt geometriskt objekt i tredimensionellt utrymme som visas överallt från sportbollar till planeter i rymden .. Låt oss använda sfären primitiv för att skapa ett nät.
Kodexemplet nedan konverterar en sfär till mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Konvertera en ruta till mesh**
I rutan beskrivs en mängd olika behållare och behållare för permanent användning som lagring eller för tillfällig användning. ofta för transport av innehåll. Låt oss använda Box primitivet för att skapa ett nät. Exempel på koden nedan omvandlar en ruta till mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Konvertera ett plan till mesh**
Ett plan sträcker sig oändligt utan tjocklek. Ett exempel på ett plan är ett koordinatplan. Låter använda `Plane` primitive för att skapa en mesh. Kodeexemplet nedan konverterar en `Plane` till `Mesh`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Konvertera en cylinder till mesh**
En cylinder är en av de mest grundläggande kurvorna geometriska formerna, den yta som bildas av punkterna på ett fast avstånd från en viss rät linje, cylinderns axel. Den kan användas på många ställen, t.ex. som en pelare framför ett hem eller som en bildrivräkt. Låt oss använda Cylinder primitivet för att skapa en mesh. Kodexemplet nedan konverterar en cylinder till mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Konvertera en Torus till mesh**
En torus är en yta av revolution som skapas genom att rotera en cirkel i tredimensionellt utrymme om en axel koplanar med cirkeln .. Om revolutionens axel inte rör cirkeln, har ytan en ringform och kallas en torus av revolution. Låt oss använda Torus primitivet för att skapa ett nät. Kodexemplet nedan konverterar en Torus till mesh.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
