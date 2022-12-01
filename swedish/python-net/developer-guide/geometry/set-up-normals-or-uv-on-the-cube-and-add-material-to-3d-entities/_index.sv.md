---
title: Ställ in normala eller UV på kuben och Lägg till material till 3D Enheter
type: docs
weight: 20
url: /sv/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Hur man skapar normala eller uv data på en mesh i Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D för Python via .NET erbjuder att hantera normala och UV på de geometriska formerna. En mesh lagrar nyckelegenskaperna för varje vertex är dess position i rymden och dess normala, en vektor vinkelrätt mot den ursprungliga ytan. Normalt är stort till skuggningsräkningar. Normalerna bör vara enhetsvektorer. De flesta mesh-format stöder också någon form av UV-koordinater som är en separat 2d-representation av mesh "ofolded" för att visa vilken del i en 2-dimensionell texturkart för olika polygoner i masken.

{{% /alert %}} {{% alert color="primary" %}}

Klassobjektet `Mesh` används i koden. Vi kan det.[Skapa ett klassobjekt `Mesh` som berättas där.](/3d/sv/python-net/create-3d-mesh-and-scene/)Och sedan peka nod till Mesh geometri vikten[Skapa en scen 3D](/3d/sv/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Skapa normala vektorer**
För att ha en bra visuell utseende på belysning, måste vi specificera normaler information för varje vertex, att ha en bättre detaljer, vi kan också använda normal och diffus karta (säkra att du kan använda skugga / spekulär karta) för att utföra per-pixel normal/färg. En per-vertex information som normal eller vertex färg uppnås `VertexElement`. I Aspose.3D kan vi kartlägga extra information till kontrollpunkter/polygon vertex/polygon/kant, ett prov för att definiera normaler för vertex:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

De 8 normala vektorerna är mappade till 8 styrpunkter direkt, i nästa exempel, kommer vi att demonstrera lite mer komplext scenario.
## **Skapa UV- koordinater**
Här har vi endast definierat 4 UV-koordinater, men tillämpade dem till 24 polygon hörn (6 face * 4 vertex per polygon) genom att använda index.
Aspose.3D ger 5 kartläggningslägen:

- `CONTROL_POINT` - varje data kartläggs till geometrins styrpunkt.
- `POLYGON_VERTEX` - uppgifterna är kartlagt till polygonens vertex.
- `POLYGON` - uppgifterna är kartlagt till polygonen.
- `EDGE` - Uppgifterna är karterade till kanten.
- `ALL_SAME` - en data som kartläggs till hela geometrin.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
## **Lägg till material till 3D Objekt**
Aspose.3D för Python via .NET gör det möjligt för utvecklare att använda skuggaalgoritm för exakt skuggning och höjdpunkter. Phong har flera karta ingångar som vi kan använda för att dölja effekten till noden. Fysiskt baserad rendering (PBR) tar hänsyn till vissa fysiska egenskaper hos objekt, ett sådant tillvägagångssätt ger utseendet av material som i den verkliga världen.
### **Phong Material med textur för kub**
När UV-koordinaterna är färdiga att använda, kan vi applicera en textur på ytan av nät med hjälp av material. Endast vertex färg kan inte beskriva ytans detaljer, det är vad material används för. Här är ett exempel för att bifoga ett Phong-material till kubennoden:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

Vi specificerade den diffusa texturkartläggningen, och en spekulär färg med en lysande parameter.
### **Applicera fysiskt baserat renderingsmaterial (PBR) på en låd**
PBR spelar en nyckelroll för spelmotorns visuella, med sin effektiva och realistiska återgivning av växelverkan mellan ljus och yta genom att dämpa ljusstyrkan och spridning av reflekterat ljus. .. Utvecklare kan använda Aspose.3D API för att applicera PBR material till 3D objekt i en scen. Detta kodexempel visar hur man skapar ett Box-objekt och sedan tillämpar PBR-materialet.

**.NET, C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
