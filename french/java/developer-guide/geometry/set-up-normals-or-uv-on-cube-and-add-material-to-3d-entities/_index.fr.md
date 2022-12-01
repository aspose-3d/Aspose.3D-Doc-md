---
title: Configurez des normales ou des UV sur Cube et ajoutez du matériel aux entités 3D
type: docs
weight: 60
url: /fr/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java propose de gérer les normales et les UV sur les formes géométriques. Un maillage stocke les propriétés clés de chaque sommet, position dans l'espace et sa normale, appelée vecteur perpendiculaire à la surface d'origine. La normale est majeure pour les comptes d'ombrage et devrait être un vecteur unitaire. La plupart des formats de maillage prennent également en charge une certaine forme de coordonnées UV qui sont une représentation 2D distincte du maillage «déplié» pour montrer quelle partie d'une carte de texture bidimensionnelle appliquer à différents polygones du maillage.
---
{{% alert color="primary" %}}

Aspose.3D for Java propose de gérer les normales et les UV sur les formes géométriques. Un maillage stocke les propriétés clés de chaque sommet, position dans l'espace et sa normale, appelée vecteur perpendiculaire à la surface d'origine. La normale est majeure pour les comptes d'ombrage et devrait être un vecteur unitaire. La plupart des formats de maillage prennent également en charge une certaine forme de coordonnées UV qui sont une représentation 2D distincte du maillage «déplié» pour montrer quelle partie d'une carte de texture bidimensionnelle appliquer à différents polygones du maillage.

{{% /alert %}} {{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons[Créer un objet de classe Mesh comme raconté ici](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Puis pointez le nœud vers la géométrie Mesh en créant une scène 3D.

{{% /alert %}}
## **Créer des vecteurs normaux**
Afin d'avoir une bonne apparence visuelle sur l'éclairage, nous devons spécifier des informations normales pour chaque sommet. Afin d'avoir les meilleurs détails, nous pouvons également utiliser une carte normale et diffuse (utilisez une carte ombre/spéculaire) pour effectuer une normale/couleur par pixel. Une information par sommet comme la couleur normale ou de sommet est obtenue par VertexElement. Au Aspose.3D, nous pouvons mapper des informations supplémentaires pour contrôler les points/polygone vertex/polygone/arête, un échantillon pour définir les normales pour le sommet:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


Les 8 vecteurs normaux sont mappés directement à 8 points de contrôle, dans l'exemple suivant, nous allons démontrer un scénario un peu plus complexe.
## **Créer des coordonnées UV**
Ici, nous n'avons défini que 4 coordonnées UV, mais les avons appliquées à 24 sommets polygonaux (6 face * 4 sommets par polygone) en utilisant des indices.
Le Aspose.3D fournit 5 modes de cartographie:

- **ControlPoint**-Chaque donnée est mappée au point de contrôle de la géométrie.
- **PolygonVertex**-Les données sont mappées au sommet du polygone.
- **Polygone**-Les données sont mappées au polygone.
- **Bord**-Les données sont mappées au bord.
- **AllSame**-Une donnée mappée à l'ensemble de la géométrie.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
## **Ajouter des matériaux aux objets 3D**
Aspose.3D for Java permet aux développeurs d'utiliser un algorithme d'ombrage pour un ombrage précis et des surlignements. Le Phong a plusieurs entrées de carte que nous pouvons utiliser pour masquer l'effet au nœud. Le rendu physique (PBR) prend en compte certaines propriétés physiques des objets, une telle approche fournit l'apparence des matériaux comme dans le monde réel.
### **Matériau Phong avec texture pour cube**
Lorsque les coordonnées UV sont prêtes à l'emploi, nous pouvons appliquer une texture sur la surface du maillage en utilisant du matériel. Seule la couleur du sommet ne peut pas décrire les détails de la surface, c'est à cela que servent les matériaux. Voici un exemple pour attacher un matériau Phong au nœud cube:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


Nous avons spécifié le mappage de texture diffuse et une couleur spéculaire avec un paramètre de brillante.
### **Appliquer du matériel de rendu à base physique (PBR) à une boîte**
PBR joue un rôle clé pour les visuels du moteur de jeu, avec son rendu efficace et réaliste des interactions entre la lumière et la surface via l'atténuation de la luminosité et la diffusion de la lumière réfléchie. Les développeurs peuvent utiliser Aspose.3D API pour appliquer du matériel PBR à 3D objets dans une scène. Cet exemple de code montre comment créer un objet Box, puis appliquer le matériau PBR.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
