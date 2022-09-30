---
title: Ställ in normalar eller UV på Cube och Lägg till material till 3D Enheter
type: docs
weight: 60
url: /sv/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java erbjuder att hantera normala och UV på de geometriska formerna. En mesh lagrar nyckelegenskaperna för varje vertex, position i rymden, och dess normala, känd som en vektor vinkelrätt mot den ursprungliga ytan. Normalt är stort till skuggningsräkningar och bör vara en enhetsvektor. De flesta mesh-format stöder också någon form av UV-koordinater som är en separat 2D-representation av mesh "ofolded" för att visa vilken del i en 2-dimensionell texturkart för olika polygoner i masken.
---
{{% alert color="primary" %}}

Aspose.3D for Java erbjuder att hantera normala och UV på de geometriska formerna. En mesh lagrar nyckelegenskaperna för varje vertex, position i rymden, och dess normala, känd som en vektor vinkelrätt mot den ursprungliga ytan. Normalt är stort till skuggningsräkningar och bör vara en enhetsvektor. De flesta mesh-format stöder också någon form av UV-koordinater som är en separat 2D-representation av mesh "ofolded" för att visa vilken del i en 2-dimensionell texturkart för olika polygoner i masken.

{{% /alert %}} {{% alert color="primary" %}}

Klassobjektet `Mesh` används i koden. Vi kan det.[Skapa ett mesh klassobjekt som berättat här.](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Och sedan peka nod till Mesh geometri genom att skapa en 3D Scene.

{{% /alert %}}
## **Skapa normala vektorer**
För att ha en bra visuell utseende på belysning, måste vi specificera normaler information för varje vertex. För att få bättre detaljer kan vi också använda normal och diffus karta (använd skugg/spekulär karta) att utföra per-pixel normal/färg. En per-vertex information som normal eller vertex färg uppnås av VertexElement. I Aspose.3D kan vi kartlägga extra information till kontrollpunkter/polygon vertex/polygon/kant, ett prov för att definiera normaler för vertex:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


De 8 normala vektorerna är mappade till 8 styrpunkter direkt, i nästa exempel, kommer vi att demonstrera lite mer komplext scenario.
## **Skapa UV- koordinater**
Här har vi endast definierat 4 UV-koordinater, men tillämpade dem till 24 polygon hörn (6 face * 4 vertex per polygon) genom att använda index.
Aspose.3D ger 5 kartläggningslägen:

- **Kontrollpunkter**- Varje data kartläggs till geometrins styrpunkt.
- **PolygonVertex**- Uppgifterna är karterade till polygonens vertex.
- **PolygonName**- Uppgifterna ska kartläggas till polygonen.
- **Kant**- Uppgifterna är karterade till kanten.
- **Allt samma**- En data som är kartlagt till hela geometrin.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
## **Lägg till material till 3D Objekt**
Aspose.3D for Java gör det möjligt för utvecklare att använda skuggaalgoritm för exakt skuggning och höjdpunkter. Phong har flera karta ingångar som vi kan använda för att dölja effekten till noden. Fysiskt baserad rendering (PBR) tar hänsyn till vissa fysiska egenskaper hos objekt, ett sådant tillvägagångssätt ger utseendet av material som i den verkliga världen.
### **Phong Material med textur för kub**
När UV-koordinaterna är färdiga att använda, kan vi applicera en textur på ytan av nät med hjälp av material. Endast vertex färg kan inte beskriva ytans detaljer, det är vad material används för. Här är ett exempel för att bifoga ett Phong-material till kubennoden:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


Vi specificerade den diffusa texturkartläggningen, och en spekulär färg med en lysande parameter.
### **Applicera fysiskt baserat renderingsmaterial (PBR) på en låd**
PBR spelar en nyckelroll för spelmotorns visuella, med sin effektiva och realistiska återgivning av växelverkan mellan ljus och yta genom att dämpa ljusstyrkan och spridning av reflekterat ljus. .. Utvecklare kan använda Aspose.3D API för att applicera PBR material till 3D objekt i en scen. Detta kodexempel visar hur man skapar ett Box-objekt och sedan tillämpar PBR-materialet.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
