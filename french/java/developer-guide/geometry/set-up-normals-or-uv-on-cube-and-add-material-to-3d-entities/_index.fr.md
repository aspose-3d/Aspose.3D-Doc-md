---
title: Configurer des normales ou des UV sur Cube et ajouter du matériel aux entités 3D
type: docs
weight: 60
url: /fr/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java propose de gérer les normales et les UV sur les formes géométriques. Un maillage stocke les propriétés clés pour chaque sommet, sa position dans l'espace et sa normale, appelée vecteur perpendiculaire à la surface d'origine. La normale est importante pour les comptes d'ombrage et devrait être un vecteur unitaire. La plupart des formats de maillage prennent également en charge une certaine forme de coordonnées UV qui sont une représentation 2D distincte du maillage "déplié" pour montrer quelle partie d'une carte de texture bidimensionnelle appliquer à différents polygones du maillage.
---
{{% alert color="primary" %}}

Aspose.3D for Java propose de gérer les normales et les UV sur les formes géométriques. Un maillage stocke les propriétés clés pour chaque sommet, sa position dans l'espace et sa normale, appelée vecteur perpendiculaire à la surface d'origine. La normale est importante pour les comptes d'ombrage et devrait être un vecteur unitaire. La plupart des formats de maillage prennent également en charge une certaine forme de coordonnées UV qui sont une représentation 2D distincte du maillage "déplié" pour montrer quelle partie d'une carte de texture bidimensionnelle appliquer à différents polygones du maillage.

{{% /alert %}} {{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh comme raconté ici](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/), puis pointer le nœud vers la géométrie Mesh en créant une scène 3D.

{{% /alert %}}
##  **Créer des vecteurs normaux**
Afin d'avoir un bon aspect visuel sur l'éclairage, nous devons spécifier des informations de normales pour chaque sommet. Afin d'avoir les meilleurs détails, nous pouvons également utiliser la carte normale et diffuse (utiliser la carte d'ombre/spéculaire) pour effectuer la normale/couleur par pixel. Une information par sommet comme la couleur normale ou vertex est obtenue par VertexElement. Dans Aspose.3D, nous pouvons mapper des informations supplémentaires aux points de contrôle/polygone vertex/polygone/edge, un exemple pour définir les normales pour vertex:

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


Les 8 vecteurs normaux sont mappés directement à 8 points de contrôle, dans l'exemple suivant, nous allons démontrer un scénario un peu plus complexe.
##  **Créer des coordonnées UV**
Ici, nous n'avons défini que 4 coordonnées UV, mais les avons appliquées à 24 sommets polygonaux (6 face * 4 sommets par polygone) en utilisant des indices.
Le Aspose.3D fournit 5 modes de mappage:

- **ControlPoint**-Chaque donnée est mappée au point de contrôle de la géométrie.
- **PolygonVertex**-Les données sont mappées au sommet du polygone.
- **Polygone**-Les données sont mappées au polygone.
- **Bord**-Les données sont mappées au bord.
- **AllSame**-Une donnée mappée à l'ensemble de la géométrie.



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
##  **Ajouter des matériaux aux objets 3D**
Aspose.3D for Java permet aux développeurs d'utiliser l'algorithme d'ombrage pour un ombrage et des reflets précis. Le Phong a plusieurs entrées de carte que nous pouvons utiliser pour masquer l'effet au noeud. Physically Based Rendering (PBR) prend en compte certaines propriétés physiques des objets, une telle approche fournit l'apparence des matériaux comme dans le monde réel.
###  **Matériau Phong avec texture pour cube**
Lorsque les coordonnées UV sont prêtes à l'emploi, nous pouvons appliquer une texture sur la surface du maillage en utilisant du matériel. Seule la couleur du sommet ne peut pas décrire les détails de la surface, c'est à cela que servent les matériaux. Voici un exemple pour attacher un matériau Phong au nœud cube:

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


Nous avons spécifié le mappage de texture diffuse et une couleur spéculaire avec un paramètre de brillante.
###  **Appliquer du matériel de rendu à base physique (PBR) à une boîte**
PBR joue un rôle clé pour les visuels du moteur de jeu, avec son rendu efficace et réaliste des interactions entre la lumière et la surface via l'atténuation de la luminosité et la diffusion de la lumière réfléchie. Les développeurs peuvent utiliser Aspose.3D API pour appliquer du matériel PBR aux objets 3D dans une scène. Cet exemple de code montre comment créer un objet Box, puis appliquer le matériau PBR.

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
