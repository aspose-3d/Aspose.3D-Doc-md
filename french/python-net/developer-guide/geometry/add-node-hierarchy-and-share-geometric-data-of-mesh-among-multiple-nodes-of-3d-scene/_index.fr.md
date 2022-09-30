---
title: Ajouter la hiérarchie des nœuds et partager les données géométriques du maillage entre plusieurs nœuds de la scène 3D
type: docs
weight: 40
url: /fr/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D pour Python via .NET propose de construire une hiérarchie de nœud. Le nœud est un élément de base d'une scène. Une hiérarchie de nœuds définit la structure logique d'une scène et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
---
## **Ajouter la hiérarchie du nœud dans le document de scène 3D**
Aspose.3D pour Python via .NET propose de construire une hiérarchie de nœud. Le nœud est un élément de base d'une scène. Une hiérarchie de nœuds définit la structure logique d'une scène et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
### **Exemple de graphique de scène**
Un exemple de hiérarchie de scène ressemble à:

![Todo: image_Alt_Texte](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

Dans Aspose.3D, chaque instance `Node` peut avoir plusieurs nœuds enfants, dans cet exemple, nous avons créé un nœud avec deux nœuds cubes, si nous faisons pivoter le nœud racine, tous les nœuds enfants sont également affectés:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
## **Partager les données de géométrie du maillage entre plusieurs nœuds**
Pour diminuer les nécessités de la mémoire, une seule instance de la classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) peut être liée à diverses instances de la classe [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node). Envisagez que vous avez besoin d'un système où tous les cubes 3D semblaient indiscernables, mais vous avez exigé de nombreux un grand nombre d'entre eux. Vous pouvez épargner la mémoire en fabriquant un objet Mesh lorsque le système démarre. À ce moment-là, chaque fois que vous avez besoin d'une autre forme, vous faites un autre objet Node, puis pointez ce nœud vers un Mesh. C'est ce qu'on appelle l'instancing. Aspose.3D pour Python via .NET Les API permettent de faire l'instancing.
### **Exemple d'instantanement**
Dans les jeux RTS (stratégie en temps réel) comme, nous pouvons toujours voir plusieurs PNJ (caractère non joueur) avec le même modèle 3D, peut-être dans des couleurs différentes, le moteur de rendu partage généralement les mêmes données de géométrie de maillage sur différents PNJ, cette technique est appelée Instenancing.

{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons[Créer un objet de classe `Mesh` tel qu'il y est raconté](/3d/fr/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Démonstration de l'exemple de code:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

Dans cet exemple, nous avons créé 3 nœuds cubes partagent le même maillage, chacun d'eux a un matériau différent avec des couleurs différentes.
