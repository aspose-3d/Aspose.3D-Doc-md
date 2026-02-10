---
title: Convertir la maille en maille triangulaire et la forme primitive en maille
type: docs
weight: 30
url: /fr/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API permet aux développeurs de convertir n'importe quel objet maillage en maillage triangulaire avec une disposition mémoire personnalisée du sommet. La disposition de mémoire personnalisée du sommet est définie à l'aide de la classe Struct ou dynamiquement par VertexDeclaration dans les exemples de code.
---
##  **Convertir un maillage en maillage Triangle avec la disposition de mémoire personnalisée du Vertex**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API permet aux développeurs de convertir n'importe quel objet maillage en maillage triangulaire avec une disposition de mémoire personnalisée du sommet. La disposition de mémoire personnalisée du sommet est définie à l'aide de la classe Struct ou dynamiquement par [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) dans les exemples de code.

{{% alert color="primary" %}}

Cette rubrique d'aide crée des maillages à partir de la boîte et de la sphère pour garder le code complet et court. Les développeurs peuvent construire un maillage manuellement comme rapporté dans cette rubrique d'aide: [Créer un maillage de cube 3D](/3d/fr/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Ces exemples montrent comment:

- [Convertir une sphère en maille triangle avec une disposition de mémoire personnalisée du sommet (défini dans le Struct)](/3d/fr/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convertir une boîte en Triangle Mesh avec une disposition de mémoire personnalisée du sommet (définie par la classe VertexDeclaration)](/3d/fr/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convertir Maille**
Les développeurs peuvent convertir le maillage en maillage triangulaire car toute structure complexe (surface) peut être représentée comme un tas de triangles. Le triangle est la géométrie la plus atomique. Ainsi, il est utilisé comme base pour presque tout.
###  **Les sommets d'accès d'un maillage Triangle**
Les développeurs peuvent accéder aux indices, aux sommets réels, aux sommets avant la fusion et au total des octets de sommets en mémoire.

L'exemple ci-dessous convertit une sphère en maillage triangle avec une disposition de mémoire personnalisée.

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




Ci-dessous, l'exemple convertit une boîte en maillage triangle avec une disposition de mémoire personnalisée.

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
##  **Convertir le Primitif en Maille**
En utilisant Aspose.3D for .NET, les développeurs peuvent convertir n'importe quel objet primitif en un maillage. Les primitives comprennent plusieurs des objets les plus basiques et les plus utilisés comme la boîte, la sphère, le plan, le cylindre et le tore.

{{% alert color="primary" %}}

Toute classe qui implémente une interface `IMeshConvertible` peut être convertie en maillage lors de l'exportation vers n'importe quel format de fichier 3D.

{{% /alert %}}
###  **Convertir une sphère en maillage**
Une sphère est un objet géométrique parfaitement rond dans un espace tridimensionnel qui apparaît partout, des balles de sport aux planètes dans l'espace. Utilisons la Sphère primitive pour créer un maillage.
L'exemple de code ci-dessous convertit une sphère en maillage.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
            
// Convert a Sphere to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir une boîte en maillage**
Une boîte décrit une variété de conteneurs et de récipients pour une utilisation permanente comme stockage, ou pour une utilisation temporaire, souvent pour le transport du contenu. Utilisons la boîte primitive pour créer un maillage. L'exemple de code ci-dessous convertit une boîte en maillage.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir un avion en maillage**
Un plan s'étend à l'infini sans épaisseur. Un exemple de plan est un plan de coordonnées. Utilisons la primitive `Plane` pour créer un maillage. L'exemple de code ci-dessous convertit un `Plane` en `Mesh`.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
            
// Convert a Plane to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir un cylindre en maille**
Un cylindre est l'une des formes géométriques curvilignes les plus élémentaires, la surface formée par les points à une distance fixe d'une ligne droite donnée, l'axe du cylindre. Il peut être utilisé dans de nombreux endroits, par exemple comme pilier devant une maison ou comme arbre de transmission de voiture. Permet d'utiliser le cylindre primitif pour créer un maillage. L'exemple de code ci-dessous convertit un cylindre en maillage.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
            
// Convert a Cylinder to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
###  **Convertir un Torus en Maille**
Un tore est une surface de révolution générée en faisant tourner un cercle dans un espace tridimensionnel autour d'un axe coplanaire avec le cercle. Si l'axe de révolution ne touche pas le cercle, la surface a une forme d'anneau et s'appelle un tore de révolution. Utilisons le Torus primitif pour créer un maillage. L'exemple de code ci-dessous convertit un Torus en maillage.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
            
// Convert a Torus to Mesh
Mesh mesh = convertible.ToMesh();

{{< /highlight >}}
