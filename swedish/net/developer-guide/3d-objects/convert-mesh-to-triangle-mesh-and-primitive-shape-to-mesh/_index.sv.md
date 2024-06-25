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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.cs" >}}




Nedan konverterar exempel en Box till triangel mesh med anpassad minnes layout.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.cs" >}}
##  **Omvandla det primitiva till ett tåg**
Med Aspose.3D for .NET kan utvecklare konvertera vilket primitivt objekt till ett mesh. Primitiv omfattar många av de mest grundläggande och mest använda föremål som låda, sfär, plan, cylinder och torus.

{{% alert color="primary" %}}

Any class that implements an interface `IMeshConvertible` can be converted to mesh while exporting to any 3D file format.

{{% /alert %}}
###  **Konvertera en sfär till mesh**
En sfär är ett perfekt rundt geometriskt objekt i tredimensionellt utrymme som visas överallt från sportbollar till planeter i rymden .. Låt oss använda sfären primitiv för att skapa ett nät.
Kodexemplet nedan konverterar en sfär till mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.cs" >}}
###  **Konvertera en ruta till mesh**
I rutan beskrivs en mängd olika behållare och behållare för permanent användning som lagring eller för tillfällig användning. ofta för transport av innehåll. Låt oss använda Box primitivet för att skapa ett nät. Exempel på koden nedan omvandlar en ruta till mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.cs" >}}
###  **Konvertera ett plan till mesh**
Ett plan sträcker sig oändligt utan tjocklek. Ett exempel på ett plan är ett koordinatplan. Låter använda `Plane` primitive för att skapa en mesh. Kodeexemplet nedan konverterar en `Plane` till `Mesh`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.cs" >}}
###  **Konvertera en cylinder till mesh**
En cylinder är en av de mest grundläggande kurvorna geometriska formerna, den yta som bildas av punkterna på ett fast avstånd från en viss rät linje, cylinderns axel. Den kan användas på många ställen, t.ex. som en pelare framför ett hem eller som en bildrivräkt. Låt oss använda Cylinder primitivet för att skapa en mesh. Kodexemplet nedan konverterar en cylinder till mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.cs" >}}
###  **Konvertera en Torus till mesh**
En torus är en yta av revolution som skapas genom att rotera en cirkel i tredimensionellt utrymme om en axel koplanar med cirkeln .. Om revolutionens axel inte rör cirkeln, har ytan en ringform och kallas en torus av revolution. Låt oss använda Torus primitivet för att skapa ett nät. Kodexemplet nedan konverterar en Torus till mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.cs" >}}
