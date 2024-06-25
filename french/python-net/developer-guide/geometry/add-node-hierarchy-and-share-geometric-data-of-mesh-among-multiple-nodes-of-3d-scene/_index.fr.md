---
title: Ajouter une hiérarchie de nœud et partager des données géométriques de maillage entre plusieurs nœuds de la scène 3D
type: docs
weight: 40
url: /fr/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET propose de construire une hiérarchie de nœuds. Le nœud est le bloc de construction de base d'une scène. Une hiérarchie de nœuds définit la structure logique d'une scène et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
---
##  **Ajouter une hiérarchie de nœud dans le document de scène 3D**
Aspose.3D for Python via .NET propose de construire une hiérarchie de nœuds. Le nœud est le bloc de construction de base d'une scène. Une hiérarchie de nœuds définit la structure logique d'une scène et fournit un contenu visible en attachant des géométries, des lumières et des caméras aux nœuds.
###  **Exemple de graphique de scène**
Un exemple de hiérarchie de scène ressemble à:

! [Tout le monde: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

Dans Aspose.3D, chaque instance `Node` peut avoir plusieurs nœuds enfants, dans cet exemple, nous avons créé un nœud avec deux nœuds cubes, si nous faisons pivoter le nœud racine, tous les nœuds enfants sont également affectés:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
##  **Partager les données de géométrie du maillage entre plusieurs nœuds**
Pour diminuer les nécessités de mémoire, une seule instance de [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class peut être liée à diverses instances de [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Envisagent que vous avez besoin d'un système où tous les 3D cubes semblaient être indiscernables, mais vous en aviez besoin d'un grand nombre. Vous pouvez épargner de la mémoire en faisant un objet Mesh lorsque le système démarre. À ce stade, chaque fois que vous avez besoin d'une autre forme, vous faites un autre objet Node, puis pointez ce nœud vers le maillage. C'est ce que l'on appelle l'instanciation. Les API Aspose.3D for Python via .NET permettent de faire l'instanciation.
###  **Exemple d'instantanement**
Dans les jeux RTS (stratégie en temps réel) comme, nous pouvons toujours voir plusieurs PNJ (personnage non joueur) avec le même modèle 3D, peut-être dans des couleurs différentes, le moteur de rendu partage généralement les mêmes données de géométrie de maillage à travers différents PNJ, cette technique s'appelle Instancing.

{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe `Mesh` comme raconté là](/3d/fr/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Démonstration de l'exemple de code:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

Dans cet exemple, nous avons créé 3 nœuds cubes partagent le même maillage, chacun d'eux a un matériau différent avec des couleurs différentes.
