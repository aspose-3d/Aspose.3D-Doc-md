---
title: Konvertera Mesh till triangel Mesh och Primitive Form till mesh
type: docs
weight: 30
url: /sv/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D för Python via .NET API gör det möjligt för utvecklare att konvertera alla mesh objekt till triangelnät med anpassad minne Vertexens layout. Vertex egen layout definieras med Struct eller dynamiskt av VertexDeclaration klass i co. Ge exempel.
---
## **Konvertera en mesh till triangeln mesh med egna minneslayout för vertex**
[Aspose.3D för Python via .NET](https://products.aspose.com/3d/python-net/)API tillåter utvecklare att konvertera någon mesh objekt till triangeln mesh med anpassad minne layout av vertex. Den anpassade minnes layouten av Vertex definieras med hjälp av Struct eller dynamiskt av [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration) klass i co. Ge exempel.

{{% alert color="primary" %}}

Detta hjälpämne skapar meshes från lådan och sfären för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt enligt berättelsen i detta hjälpämne:[Skapa en 3D Cube mesh](/3d/sv/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Dessa exempel visar hur:

- [Konvertera en sfär till triangeln Mesh med anpassad layout av vertex (definierad i Struct)](/3d/sv/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Konvertera en ruta till triangeln Mesh med egen layout av vertex (definierad av VertexDeclaration klass)](/3d/sv/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Konvertera mask**
Utvecklare kan konvertera mesh till triangeln mesh eftersom alla komplexa (yta) strukturer kan representeras som ett gäng trianglar. Triangeln är den mest atomiska geometrin. Således används den som bas för nästan allt.
### **Åtkomst hörn av en triangel Mesh**
Utvecklare kan komma åt index, faktiska hörn, hörn före sammanslagning och total byte av hörn i minnet.

Nedan konverterar exempel en Sfär till triangeln mesh med anpassad minne layout.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




Nedan konverterar exempel en Box till triangel mesh med anpassad minnes layout.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
## **Konvertera 'primitiv' till en 'Mesh'**
Med Aspose.3D för Python via .NET kan utvecklare konvertera alla primitiva objekt till en mesh. Primitiv omfattar många av de mest grundläggande och mest använda föremål som låda, sfär, plan, cylinder och torus.

{{% alert color="primary" %}}

Alla klasser som implementerar ett gränssnitt IMeshConvertible kan konverteras till mesh när du exporterar till 3D filformat.

{{% /alert %}}
### **Konvertera ett 'Sphere' till 'Mesh'**
En sfär är ett perfekt rundt geometriskt objekt i tredimensionellt utrymme som visas överallt från sportbollar till planeter i rymden .. Låt oss använda sfären primitiv för att skapa ett nät.
Kodexemplet nedan konverterar en sfär till mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.py" >}}
### **Konvertera en 'ruta' till 'Mesh'**
I rutan beskrivs en mängd olika behållare och behållare för permanent användning som lagring eller för tillfällig användning. ofta för transport av innehåll. Låt oss använda Box primitivet för att skapa ett nät. Exempel på koden nedan omvandlar en ruta till mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.py" >}}
### **Konvertera en 'Plane' till 'Mesh'**
Ett plan sträcker sig oändligt utan tjocklek. Ett exempel på ett plan är ett koordinatplan. Låt oss använda planet primitivet för att skapa ett nät. Kodexemplet nedan konverterar ett plan till mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.py" >}}
### **Konvertera en 'cylinder' till 'Mesh'**
En cylinder är en av de mest grundläggande kurvorna geometriska formerna, den yta som bildas av punkterna på ett fast avstånd från en viss rät linje, cylinderns axel. Den kan användas på många ställen, t.ex. som en pelare framför ett hem eller som en bildrivräkt. Låt oss använda Cylinder primitivet för att skapa en mesh. Kodexemplet nedan konverterar en cylinder till mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.py" >}}
### **Konvertera en 'Torus' till 'Mesh'**
En torus är en yta av revolution som skapas genom att rotera en cirkel i tredimensionellt utrymme om en axel koplanar med cirkeln .. Om revolutionens axel inte rör cirkeln, har ytan en ringform och kallas en torus av revolution. Låt oss använda Torus primitivet för att skapa ett nät. Kodexemplet nedan konverterar en Torus till mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.py" >}}
