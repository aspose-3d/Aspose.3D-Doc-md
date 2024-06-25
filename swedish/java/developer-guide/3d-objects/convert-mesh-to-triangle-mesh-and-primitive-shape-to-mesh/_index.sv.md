---
title: Konvertera Mesh till triangel Mesh och Primitive Form till mesh
type: docs
weight: 20
url: /sv/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API has support to convert mesh to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined dynamically by VertexDeclaration class in the code examples.
---
##  **Konvertera Mesh till triangeln Mesh med anpassad minne layout av Vertex**
Aspose.3D for Java API has support to convert mesh to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined dynamically by `VertexDeclaration` class in the code examples.

{{% alert color="primary" %}}

Detta hjälpämne skapar meshes från lådan och sfären för att hålla koden omfattande och kort. Utvecklare kan konstruera en mesh manuellt som är berättad i detta hjälpämne: [Skapa 3D kube mesh](/3d/sv/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Utvecklare kan konvertera mesh till triangeln mesh eftersom alla komplexa (yta) strukturer kan representeras som ett gäng trianglar. Triangeln är den mest atomiska geometrin. Således används den som bas för nästan allt. Detta kodexempel konverterar en ruta till triangelnät med anpassad layout.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.java" >}}
##  **Konvertera primitiv form till mesh**
Aspose.3D for Java API har stöd för att konvertera primitiv form till mesh. Primitiva former inkluderar de flesta grundläggande och begagnade föremål som box, sfär, plan, cylinder och torus.

{{% alert color="primary" %}}

Any class that implements an interface IMeshConvertible can be converted to mesh while exporting to any 3D file format.

{{% /alert %}}
###  **Konvertera sfären Primitiv till mesh**
En sfär är ett perfekt rundt geometriskt objekt i tredimensionellt utrymme som visas överallt från sportbollar till planeter i rymden .. Låt oss använda sfären primitiv för att skapa ett nät.
Kodexemplet nedan konverterar en sfär till mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertSpherePrimitivetoMesh.java" >}}
###  **Konvertera ruta till mesh**
I rutan beskrivs en mängd olika behållare och behållare för permanent användning som lagring eller för tillfällig användning. ofta för transport av innehåll. Låt oss använda Box primitivet för att skapa ett nät. Exempel på koden nedan omvandlar en ruta till mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxPrimitivetoMesh.java" >}}
###  **Konvertera ett plan till mesh**
Ett plan sträcker sig oändligt utan tjocklek. Ett exempel på ett plan är ett koordinatplan. Låt oss använda planet primitivet för att skapa ett nät. Kodexemplet nedan konverterar ett plan till mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertPlanePrimitivetoMesh.java" >}}
###  **Konvertera en cylinder till mesh**
En cylinder är en av de mest grundläggande kurvorna geometriska formerna, den yta som bildas av punkterna på ett fast avstånd från en viss rät linje, cylinderns axel. Den kan användas på många ställen, t.ex. som en pelare framför ett hem eller som en bildrivräkt. Låt oss använda Cylinder primitivet för att skapa en mesh. Kodexemplet nedan konverterar en cylinder till mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertCylinderPrimitivetoMesh.java" >}}
###  **Konvertera en Torus till mesh**
En torus är en yta av revolution som skapas genom att rotera en cirkel i tredimensionellt utrymme om en axel koplanar med cirkeln .. Om revolutionens axel inte rör cirkeln, har ytan en ringform och kallas en torus av revolution. Låt oss använda Torus primitivet för att skapa ett nät. Kodexemplet nedan konverterar en Torus till mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertTorusPrimitivetoMesh.java" >}}
