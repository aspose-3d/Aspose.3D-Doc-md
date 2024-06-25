---
title: "Offentlig API Ändrar i Aspose.3D 1.5.0 @ info: whatsthis"
type: docs
weight: 20
url: /sv/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Innehåll**

- [Convert the Primitive to a Mesh and Create a Scene from Primitive 3D Models](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convert a Mesh to Triangle Mesh with Custom Memory Layout of the Vertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Split Mesh](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Removal of Distreet3DS format.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Adds Discreet3DS format.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 1.4.0 till 1.5.0, vilket kan vara av intresse för modul-/programutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Konvertera det primitiva till en mesh och skapa en scen från Primitive 3D Modeller**
**Olika klasser, metoder och egenskaper läggs till.**

- **Lägger till gränssnitt Aspose.ThreeD.Entites.IMeshConvertible.** 
  - Any class that implements this interface can be converted to mesh while exporting to any 3D file formats.
- **Lägger till klass Aspose.ThreeD.Entites.Primitive.** 
- Den härrör från enhetsklass och även basklassen för alla primitiva klasser.
- **Lägger till klass Aspose.ThreeD.Entites.Box/Cylinder/Plane/Sphere/Torus.** 
- Dessa kan användas för att definiera scen med enkla primitiva. Utvecklare kan också konvertera dem till mesh automatiskt.

Primitiv omfattar många av de mest grundläggande och mest använda föremål som låda, sfär, plan, cylinder och torus. Utvecklare kan också konvertera dem till mesh för modifieringsändamål. Dessa hjälpämnen illustrerar hur man gör så: [Omvandla det primitiva till ett tåg](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) och [Omvandla det primitiva till ett tåg](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
###  **Konvertera en mesh till triangeln mesh med egna minneslayout för vertex**
**Olika klasser, metoder och egenskaper läggs till.**

- **Lägger till klass Aspose.ThreeD.Entites.TriMesh/TriMesh<T>** 
- TriMesh/TriMesh<T>Innehåller definitionen för triangelbaserade maskor med anpassad minneslag, vilket är användbart när utvecklaren kräver att konvertera scenen till sina egna filformat eller i rendering.
- **Lägger till struktur Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4** 
- De här klasserna visar vektorkomponenter i floaten. Endast ett fåtal moderna GPU stöder dubbel-precisionsvektor, Enkelprecisionsflödetyper är mer välkomnade i realtids renderingsvärlden. Dessa ersättningar kommer att existera samtidigt med den ursprungliga Vector2/Vector3/Vector4 eftersom de spelar olika roller i Aspose.3D. Dubbel-precision används främst för att lagra modellens data eftersom den har mindre ackumulerat fel. Single-precision används huvudsakligen i rendering eller användarens egna egenutvecklade filformat konvertering eftersom den har bättre acceptans och prestanda. Vi introducerade denna uppsättning vektorer i Aspose. 3D 1. 5 eftersom vi lagt till stöd för egen vertex layout, där floatvektorerna används ofta.
- **Lägger till attributklass Aspose.ThreeD.Utilities.SemanticAttribute** 
- Utvecklare kan definiera anpassad struktur för vertex, och använda detta attribut för att markera semantiska fält.
- **Lägger till klass Aspose. ThreeD.Utilities.VertexDeclarationName** 
- Det beskriver minnesbilden.
- **Lägger till enum Aspose ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic** 
- Dessa enumtyper annotera vertex fältets datatyp och semantisk respektive.
- **Lägger till klass Aspose.ThreeD.Utilities.VertexField.** 
- Det beskriver varje fält i den anpassade minne layouten av Vertex.
- **Lägger till klass Aspose.ThreeD.Utilities.Vertex** 
- Det kan användas för att komma åt rå vertex i TriMesh/TriMesh<T>

Utvecklare kan konvertera alla mesh objekt till triangeln mesh med den anpassade minne layout av vertex. De grafiska programvara paketen och hårdvaranheterna fungerar effektivare på trianglar. Detta hjälpämne illustrerar hur man gör så: [Konvertera en mesh till triangeln mesh med egna minneslayout för vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct).
###  **Dela mask**
**Olika klasser, metoder och egenskaper läggs till.**

- **Lägger till enum Aspose.ThreeD.Entites.SplitMeshPolicy** 
- Det specificerar datapolicyn som används i nätdelningsalgoritmen, vi stöder två policyer, Dela data mellan delar eller varje delmash har sina egna data (endast använda data).
- **Lägger till 3 SplitMesh- metoder till Aspose ThreeD.Entites.PolygonModifier Class.** 
1. Dela maskor på en specificerad nod till undermaskor efter materialdefinition.
1. Dela alla mesh i den givna scenen till undermasken efter materiell definition.
1. Dela upp den givna masken på undermaskor efter materialdefinition.
- **Lägger till egendom FlipCoordinateSystem i klass Aspose ThreeD.Formats.Universal3DConfig** 
- Det gör det möjligt för användare att vända koordinatsystemet för U3D under import eller export.

Utvecklare kan kräva att automatiskt dela en mask efter material. så att varje maska endast använder ett material eller delade maskor genom att specificera materialet. Dessa hjälpämnen illustrerar hur man gör så: [Dela ett mask genom att ange materialet](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) och [Dela alla masker av en scen per material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
###  **Avlägsnande av Distreet3DS format.**
Distreet3DS-formatet är markerat som föråldrat på grund av den felaktiga formeln.
###  **Lägger till formatet Discreet3DS.**
Discreet3DS format har introducerats.
###  **Lägger till egendom FlipCoordinateSystem i klass Aspose ThreeD.Formats.Universal3DConfig**
Det tillåter användare att vända koordinatsystemet för U3D under import eller export.
