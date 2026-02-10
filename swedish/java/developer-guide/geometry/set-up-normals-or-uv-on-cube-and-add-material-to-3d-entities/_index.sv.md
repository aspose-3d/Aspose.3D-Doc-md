---
title: Ställ in normalvärden eller UV på kuben och Lägg till material till 3D Enheter
type: docs
weight: 60
url: /sv/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java erbjuder att hantera normala och UV på de geometriska formerna. En mesh lagrar nyckelegenskaperna för varje vertex, position i rymden, och dess normala, känd som en vektor vinkelrätt mot den ursprungliga ytan. Normalt är stort till skuggningsräkningar och bör vara en enhetsvektor. De flesta mesh-format stöder också någon form av UV-koordinater som är en separat 2D-representation av mesh "ofolded" för att visa vilken del i en 2-dimensionell texturkart för olika polygoner i masken.
---
{{% alert color="primary" %}}

Aspose.3D for Java erbjuder att hantera normala och UV på de geometriska formerna. En mesh lagrar nyckelegenskaperna för varje vertex, position i rymden, och dess normala, känd som en vektor vinkelrätt mot den ursprungliga ytan. Normalt är stort till skuggningsräkningar och bör vara en enhetsvektor. De flesta mesh-format stöder också någon form av UV-koordinater som är en separat 2D-representation av mesh "ofolded" för att visa vilken del i en 2-dimensionell texturkart för olika polygoner i masken.

{{% /alert %}} {{% alert color="primary" %}}

Klassobjektet `Mesh` används i koden. Vi kan [Skapa ett mesh klassobjekt som berättat här.](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) och sedan peka nod till Mesh geometri genom att skapa en 3D scen.

{{% /alert %}}
##  **Skapa normala vektorer**
För att ha en bra visuell utseende på belysning, måste vi specificera normaler information för varje vertex. För att få bättre detaljer kan vi också använda normal och diffus karta (använd skugg/spekulär karta) att utföra per-pixel normal/färg. En per-vertex information som normal eller vertex färg uppnås av VertexElement. I Aspose. 3D kan vi kartlägga extra information till kontrollpunkter/polygon vertex/polygon/kant, ett prov för att definiera normaler för vertex:

{{< highlight "java" >}}
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}


De 8 normala vektorerna är mappade till 8 styrpunkter direkt, i nästa exempel, kommer vi att demonstrera lite mer komplext scenario.
##  **Skapa UV- koordinater**
Här har vi endast definierat 4 UV-koordinater, men tillämpade dem till 24 polygon hörn (6 face * 4 vertex per polygon) genom att använda index.
Aspose.3D tillhandahåller 5 kartläggningslägen:

- **Kontrollpunkter**- Varje data kartläggs till geometrins styrpunkt.
- **PolygonVertex**- Uppgifterna är karterade till polygonens vertex.
- **PolygonName**- Uppgifterna ska kartläggas till polygonen.
- **Kant**- Uppgifterna är karterade till kanten.
- **Allt samma**- En data som är kartlagt till hela geometrin.



{{< highlight "java" >}}
// UVs
Vector4[] uvs = new Vector4[]
{
    new Vector4( 0.0, 1.0,0.0, 1.0),
    new Vector4( 1.0, 0.0,0.0, 1.0),
    new Vector4( 0.0, 0.0,0.0, 1.0),
    new Vector4( 1.0, 1.0,0.0, 1.0)
};
// Indices of the uvs per each polygon
int[] uvsId = new int[]
{
    0,1,3,2,2,3,5,4,4,5,7,6,6,7,9,8,1,10,11,3,12,0,2,13
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Create UVset
VertexElementUV elementUV = mesh.createElementUV(TextureMapping.DIFFUSE, MappingMode.POLYGON_VERTEX, ReferenceMode.INDEX_TO_DIRECT);
// Copy the data to the UV vertex element
elementUV.setData(uvs);
elementUV.setIndices(uvsId);
{{< /highlight >}}
##  **Lägg till material till 3D Objekt**
Aspose.3D for Java tillåter utvecklare att använda skuggaalgoritm för exakt skuggning och markeringar. Phong har flera karta ingångar som vi kan använda för att dölja effekten till noden. Fysiskt baserad rendering (PBR) tar hänsyn till vissa fysiska egenskaper hos objekt, ett sådant tillvägagångssätt ger utseendet av material som i den verkliga världen.
###  **Phong Material med textur för kub**
När UV-koordinaterna är färdiga att använda, kan vi applicera en textur på ytan av nät med hjälp av material. Endast vertex färg kan inte beskriva ytans detaljer, det är vad material används för. Här är ett exempel för att bifoga ett Phong-material till kubennoden:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize cube node object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cubeNode.setEntity(mesh);
// Add cube to the scene
scene.getRootNode().addChildNode(cubeNode);
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
// Initiallize Texture object
Texture diffuse = new Texture();
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Set local file path
diffuse.setFileName(MyDir + "surface.dds");
// Set Texture of the material
mat.setTexture(Material.MAP_DIFFUSE, diffuse);
// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.setFileName("embedded-texture.png");
// Set binary content
diffuse.setContent(Files.readAllBytes(Paths.get(MyDir, "aspose-logo.jpg")));
// Set color
mat.setSpecularColor(new Vector3(1, 0, 0));
// Set brightness
mat.setShininess(100);
// Set material property of the cube object
cubeNode.setMaterial(mat);
MyDir = MyDir + RunExamples.getOutputFilePath("MaterialToCube.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


Vi specificerade den diffusa texturkartläggningen, och en spekulär färg med en lysande parameter.
###  **Applicera fysiskt baserat renderingsmaterial (PBR) på en låd**
PBR spelar en nyckelroll för spelmotorns visuella, med sin effektiva och realistiska återgivning av växelverkan mellan ljus och yta genom att dämpa ljusstyrkan och spridning av reflekterat ljus. .. Utvecklare kan använda Aspose.3D API för att applicera PBR-material på 3D-objekt i en scen. Detta kodexempel visar hur man skapar ett Box-objekt och sedan tillämpar PBR-materialet.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}
