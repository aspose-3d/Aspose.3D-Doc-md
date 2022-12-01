---
title: Configurez des normales ou des UV sur le cube et ajoutez du matériel aux entités 3D
type: docs
weight: 20
url: /fr/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Comment créer des données normales ou uv sur un maillage dans Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET propose de gérer les normales et les UV sur les formes géométriques. Un maillage stocke les propriétés clés de chaque sommet sont sa position dans l'espace et sa normale, un vecteur perpendiculaire à la surface d'origine. La normale est majeure pour les comptes d'ombrage. Les normales devraient être des vecteurs unitaires. La plupart des formats de maillage prennent également en charge une certaine forme de coordonnées UV qui sont une représentation 2d distincte du maillage "déplié" pour montrer quelle partie d'une carte de texture bidimensionnelle appliquer aux différents polygones du maillage.

{{% /alert %}} {{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons[Créer un objet de classe Mesh tel que raconté là-bas](/3d/fr/net/create-3d-mesh-and-scene/)Puis pointez le nœud vers la géométrie Mesh par[Création d'une scène 3D](/3d/fr/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Créer des vecteurs normaux**
Pour avoir un bon aspect visuel de l'éclairage, nous devons spécifier des informations normales pour chaque sommet, pour avoir de meilleurs détails, nous pouvons également utiliser une carte normale et diffuse (vous pouvez certainement utiliser une carte ombre/spéculaire) pour effectuer une normale par pixel/couleur. Une information par sommet comme la couleur normale ou de sommet est obtenue par VertexElement. Au Aspose.3D, nous pouvons mapper des informations supplémentaires pour contrôler les points/polygone vertex/polygone/arête, un échantillon pour définir les normales pour le sommet:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.cs" >}}

Les 8 vecteurs normaux sont mappés directement à 8 points de contrôle, dans l'exemple suivant, nous allons démontrer un scénario un peu plus complexe.
## **Créer des coordonnées UV**
Ici, nous n'avons défini que 4 coordonnées UV, mais les avons appliquées à 24 sommets polygonaux (6 face * 4 sommets par polygone) en utilisant des indices.
Le Aspose.3D fournit 5 modes de cartographie:

- `ControlPoint`-chaque donnée est mappée au point de contrôle de la géométrie.
- `PolygonVertex`-les données sont mappées au sommet du polygone.
- `Polygon`-les données sont mappées au polygone.
- `Edge`-les données sont mappées au bord.
- `AllSame`-une donnée mappée à l'ensemble de la géométrie.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.cs" >}}
## **Ajouter des matériaux aux objets 3D**
Aspose.3D for .NET permet aux développeurs d'utiliser un algorithme d'ombrage pour un ombrage précis et des surlignements. Le Phong a plusieurs entrées de carte que nous pouvons utiliser pour masquer l'effet au nœud. Le rendu physique (PBR) prend en compte certaines propriétés physiques des objets, une telle approche fournit l'apparence des matériaux comme dans le monde réel.
### **Matériau Phong avec texture pour cube**
Lorsque les coordonnées UV sont prêtes à l'emploi, nous pouvons appliquer une texture sur la surface du maillage en utilisant du matériel. Seule la couleur du sommet ne peut pas décrire les détails de la surface, c'est à cela que servent les matériaux. Voici un exemple pour attacher un matériau Phong au nœud cube:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.cs" >}}

Nous avons spécifié le mappage de texture diffuse et une couleur spéculaire avec un paramètre de brillante.
### **Appliquer du matériel de rendu à base physique (PBR) à une boîte**
PBR joue un rôle clé pour les visuels du moteur de jeu, avec son rendu efficace et réaliste des interactions entre la lumière et la surface via l'atténuation de la luminosité et la diffusion de la lumière réfléchie. Les développeurs peuvent utiliser Aspose.3D API pour appliquer du matériel PBR à 3D objets dans une scène. Cet exemple de code montre comment créer un objet Box, puis appliquer le matériau PBR.

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
