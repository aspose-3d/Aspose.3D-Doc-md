---
title: Ställ in normala eller UV på kuben och Lägg till material till 3D Enheter
type: docs
weight: 20
url: /sv/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Hur man skapar normala eller uv data på en mesh i Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET erbjuder att hantera normala och UV på de geometriska formerna. En mesh lagrar nyckelegenskaperna för varje vertex är dess position i rymden och dess normala, en vektor vinkelrätt mot den ursprungliga ytan. Normalt är stort till skuggningsräkningar. Normalerna bör vara enhetsvektorer. De flesta mesh-format stöder också någon form av UV-koordinater som är en separat 2d-representation av mesh "ofolded" för att visa vilken del i en 2-dimensionell texturkart för olika polygoner i masken.

{{% /alert %}} {{% alert color="primary" %}}

Klassobjektet `Mesh` används i koden. Vi kan det.[Skapa ett Mesh-klassobjekt som berättat där.](/3d/sv/net/create-3d-mesh-and-scene/)Och sedan peka nod till Mesh geometri vikten[Skapa en scen 3D](/3d/sv/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Skapa normala vektorer**
För att ha en bra visuell utseende på belysning, måste vi specificera normaler information för varje vertex, att ha en bättre detaljer, vi kan också använda normal och diffus karta (säkra att du kan använda skugga / spekulär karta) för att utföra per-pixel normal/färg. En per-vertex information som normal eller vertex färg uppnås av VertexElement. I Aspose.3D kan vi kartlägga extra information till kontrollpunkter/polygon vertex/polygon/kant, ett prov för att definiera normaler för vertex:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.cs" >}}

De 8 normala vektorerna är mappade till 8 styrpunkter direkt, i nästa exempel, kommer vi att demonstrera lite mer komplext scenario.
## **Skapa UV- koordinater**
Här har vi endast definierat 4 UV-koordinater, men tillämpade dem till 24 polygon hörn (6 face * 4 vertex per polygon) genom att använda index.
Aspose.3D ger 5 kartläggningslägen:

- `ControlPoint` - varje data kartläggs till geometrins styrpunkt.
- `PolygonVertex` - uppgifterna är kartlagt till polygonens vertex.
- `Polygon` - uppgifterna är kartlagt till polygonen.
- `Edge` - Uppgifterna är karterade till kanten.
- `AllSame` - en data som kartläggs till hela geometrin.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.cs" >}}
## **Lägg till material till 3D Objekt**
Aspose.3D for .NET gör det möjligt för utvecklare att använda skuggaalgoritm för exakt skuggning och höjdpunkter. Phong har flera karta ingångar som vi kan använda för att dölja effekten till noden. Fysiskt baserad rendering (PBR) tar hänsyn till vissa fysiska egenskaper hos objekt, ett sådant tillvägagångssätt ger utseendet av material som i den verkliga världen.
### **Phong Material med textur för kub**
När UV-koordinaterna är färdiga att använda, kan vi applicera en textur på ytan av nät med hjälp av material. Endast vertex färg kan inte beskriva ytans detaljer, det är vad material används för. Här är ett exempel för att bifoga ett Phong-material till kubennoden:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.cs" >}}

Vi specificerade den diffusa texturkartläggningen, och en spekulär färg med en lysande parameter.
### **Applicera fysiskt baserat renderingsmaterial (PBR) på en låd**
PBR spelar en nyckelroll för spelmotorns visuella, med sin effektiva och realistiska återgivning av växelverkan mellan ljus och yta genom att dämpa ljusstyrkan och spridning av reflekterat ljus. .. Utvecklare kan använda Aspose.3D API för att applicera PBR material till 3D objekt i en scen. Detta kodexempel visar hur man skapar ett Box-objekt och sedan tillämpar PBR-materialet.

**.NET, C#**

{{< highlight "java" >}}

 // initialize a scene

Scene scene = new Scene();

// initialize PBR material object

PbrMaterial mat = new PbrMaterial();

// an almost metal material

mat.MetallicFactor = 0.9;

// material surface is very rough

mat.RoughnessFactor = 0.9;

// create a box to which the material will be applied

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

// save 3d scene into STL format

scene.Save(@"C:\3D\PBR_Material_Box_Out.stl", FileFormat.STLASCII);

{{< /highlight >}}
