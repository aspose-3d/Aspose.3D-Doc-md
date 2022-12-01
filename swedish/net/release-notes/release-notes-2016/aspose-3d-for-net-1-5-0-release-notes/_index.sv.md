---
title: Aspose.3D for .NET 1.5.0 Utgivningsmeddelanden
type: docs
weight: 80
url: /sv/net/aspose-3d-for-net-1-5-0-release-notes/
---
## **Andra förbättringar och förändringar**

|**Nyckel** |**Sammanfattning** |**Kategori** |
|:- |:- |:- |
|THREEDNET-146 |Konvertera geometrier till per-vertex struktur.|Ny funktion|
|THREEDNET-148 |Tillåt användaren att dela maskor per material.|Ny funktion|
|THREEDNET-150 |Skapa nät för flygplan.|Ny funktion|
|THREEDNET-151 |Skapa nät för Box.|Ny funktion|
|THREEDNET-152 |Skapa nät för Sfären.|Ny funktion|
|THREEDNET-153 |Skapa nät för cylinder.|Ny funktion|
|THREEDNET-155 |Skapa nät för torus.|Ny funktion|
|THREEDNET-145 |Tillåt vänd koordinatsystem i U3D:s belastning/spar konfigurationsklass.|Förbättring|
|THREEDNET-154 |Stavningsproblem: Distreet3DS bör vara Discreet3DS.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se listan för eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Avlägsnande av Distreet3DS format.**
Distreet3DS-formatet är markerat som föråldrat på grund av den felaktiga formeln.
#### **Lägger till Discreet3DS format.**
Discreet3DS format har införts.
#### **Lägger till gränssnitt Aspose.ThreeD.Enheter.IMeshConvertible.**
Alla klasser som genomför detta gränssnitt kan konverteras till mesh när du exporterar till 3D filformat.
#### **Lägger till klass Aspose.ThreeD.Enheter.Primitiv.**
Den härrör från enhetsklass och även basklassen för alla primitiva klasser.
#### **Lägger till klass Aspose.ThreeD Enheter.Box/Cylinder/Plane/Sphere/Torus**
Dessa kan användas för att definiera scen med enkla primitiva. Utvecklare kan också konvertera dem till mesh automatiskt.
#### **Lägger till klass Aspose.ThreeD.Enheter.TriMesh/TriMesh<T>**
TriMesh/TriMesh<T>Innehåller definitionen för triangelbaserade maskor med anpassad minneslag, vilket är användbart när utvecklaren kräver att konvertera scenen till sina egna filformat eller i rendering.
#### **Lägger till struktur Aspose.ThreeD.Utiliteter.FVector2/FVector3/FVector4**
Dessa klasser presenterar vektorkomponenter i floaten. Endast ett fåtal moderna GPU stöder dubbel-precisionsvektor, Enkelprecisionsflödetyper är mer välkomnade i realtids renderingsvärlden. Dessa ersättare kommer att samexistera med den ursprungliga Vector2/Vector3/Vector4 eftersom de spelar olika roller i Aspose.3D. Dubbel-precision används främst för att lagra modellens data eftersom den har mindre ackumulerat fel. Single-precision används huvudsakligen i rendering eller användarens egna egenutvecklade filformat konvertering eftersom den har bättre acceptans och prestanda. Vi introducerade denna uppsättning av vektorer i Aspose.3D 1.5 eftersom vi lade till stöd för anpassade vertex layout, där flytvektorerna kommer att användas ofta.
#### **Lägger till attributklass Aspose.ThreeD.Utilities.SemanticAttribut**
Utvecklare kan definiera egna strukturer för vertex, och använda detta attribut för att markera semantiska fält.
#### **Lägger till klass Aspose.ThreeD.Utiliteter.Vertexförklaring**
Den beskriver minnesbilden av vertex.
#### **Lägger till enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic**
Dessa enumtyper noterar vertex fältets datatyp respektive semantisk.
#### **Lägger till klass Aspose.ThreeD.Utilities.VertexField**
Den beskriver varje fält i den anpassade minne layouten av Vertex.
#### **Lägger till klass Aspose.ThreeD.Utiliteter.Vertex**
Det kan användas för att komma åt rå vertex i TriMesh/TriMesh<T>
#### **Lägger till enum Aspose.ThreeD.Entites.SplitMeshPolicy**
Det specificerar datapolicyn som används i mesh splitting algoritm, vi stöder två policyr, Dela data mellan delar eller varje delmash har sina egna data (endast använda data).
#### **Lägger till 3 SplitMesh metoder till Aspose.ThreeD.Enheter.PolygonModifier klass**
1. Dela maskor på en specificerad nod till undermaskor efter materialdefinition.
1. Dela alla maskor i den givna scenen till undermaskor efter materiell definition.
1. Dela upp den givna masken på undermaskor efter materiell definition.
#### **Lägger till egendom FlipCoordinateSystem i klass Aspose.ThreeD.Formats.Universal3DConfig**
Det gör det möjligt för användare att vända koordinatsystemet U3D under import eller export.

