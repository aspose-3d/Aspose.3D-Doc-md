---
title: Ajouter la hiérarchie des nœuds et partager les données géométriques du maillage entre plusieurs nœuds de la scène 3D
type: docs
weight: 20
url: /fr/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java a l'appui de la construction d'une hiérarchie de nœuds. Le nœud est un bloc de construction de base de la scène 3D et une hiérarchie de nœuds définit la structure logique de la scène 3D et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
---
## **Ajouter la hiérarchie du nœud dans le document de scène 3D**
Aspose.3D for Java a l'appui de la construction d'une hiérarchie de nœuds. Le `Node` est un bloc de construction de base de la scène 3D et une hiérarchie de nœuds définit la structure logique de la scène 3D et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
### **Exemple de graphique de scène**

Dans Aspose.3D, chaque instance `Node` peut avoir plusieurs nœuds enfants, dans cet exemple, nous avons créé un nœud avec deux nœuds cubes, si nous faisons pivoter le nœud racine, tous les nœuds enfants sont également affectés:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
## **Partager les données de géométrie du maillage entre plusieurs nœuds**
Afin de diminuer les nécessités de la mémoire, une seule instance de la classe `Mesh` peut être liée à diverses instances de la classe `Node`. Envisagez que vous avez besoin d'un système où tous les cubes 3D semblaient indiscernables, mais vous avez exigé de nombreux un grand nombre d'entre eux. Vous pouvez épargner la mémoire en fabriquant un objet Mesh lorsque le système démarre. À ce stade, chaque fois que vous avez besoin d'une autre forme, vous faites un autre objet Node, puis pointez ce nœud vers celui `Mesh`. C'est ce qu'on appelle l'instancing. Aspose.3D for Java Les API permettent de faire l'instancing.
### **Exemple d'instantanement**
Dans les jeux RTS (stratégie en temps réel) comme, nous pouvons toujours voir plusieurs PNJ (caractère non joueur) avec le même modèle 3D, peut-être dans des couleurs différentes, le moteur de rendu partage généralement les mêmes données de géométrie de maillage sur différents PNJ, cette technique est appelée Instenancing.

{{% alert color="primary" %}} 

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons[Créer un objet de classe Mesh tel que raconté là-bas](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Démonstration de l'exemple de code:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


Dans cet exemple, nous avons créé 3 nœuds cubes partagent le même maillage, chacun d'eux a un matériau différent avec des couleurs différentes.
