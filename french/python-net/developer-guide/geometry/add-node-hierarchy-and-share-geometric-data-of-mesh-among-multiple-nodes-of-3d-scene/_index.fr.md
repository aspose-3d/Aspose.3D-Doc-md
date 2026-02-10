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

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.utilities import Quaternion, Vector3
import math

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Get a child node object
top = scene.root_node.create_child_node()
#  Each cube node has their own translation
cube1 = top.create_child_node("cube1")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the mesh
cube1.entity = mesh
#  Set first cube translation
cube1.transform.translation = Vector3(-10, 0, 0)
cube2 = top.create_child_node("cube2")
#  Point node to the mesh
cube2.entity = mesh
#  Set second cube translation
cube2.transform.translation = Vector3(10, 0, 0)
#  The rotated top node will affect all child nodes
top.transform.rotation = Quaternion.from_euler_angle(math.pi, 4, 0)
#  The path to the documents directory.
output = "out"  + "NodeHierarchy.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Partager les données de géométrie du maillage entre plusieurs nœuds**
Pour diminuer les nécessités de mémoire, une seule instance de [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class peut être liée à diverses instances de [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Envisagent que vous avez besoin d'un système où tous les 3D cubes semblaient être indiscernables, mais vous en aviez besoin d'un grand nombre. Vous pouvez épargner de la mémoire en faisant un objet Mesh lorsque le système démarre. À ce stade, chaque fois que vous avez besoin d'une autre forme, vous faites un autre objet Node, puis pointez ce nœud vers le maillage. C'est ce que l'on appelle l'instanciation. Les API Aspose.3D for Python via .NET permettent de faire l'instanciation.
###  **Exemple d'instantanement**
Dans les jeux RTS (stratégie en temps réel) comme, nous pouvons toujours voir plusieurs PNJ (personnage non joueur) avec le même modèle 3D, peut-être dans des couleurs différentes, le moteur de rendu partage généralement les mêmes données de géométrie de maillage à travers différents PNJ, cette technique s'appelle Instancing.

{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe `Mesh` comme raconté là](/3d/fr/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Démonstration de l'exemple de code:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene
from aspose.threed.shading import LambertMaterial
from aspose.threed.utilities import Vector3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Define color vectors
colors = [Vector3(1, 0, 0), Vector3(0, 1, 0), Vector3(0, 0, 1)]
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
idx = 0
for color in colors:
    #  Initialize cube node object
    cube = Node("cube")
    cube.entity = mesh
    mat = LambertMaterial()
    #  Set color
    mat.diffuse_color = color
    #  Set material
    cube.material = mat
    #  Set translation
    cube.transform.translation = Vector3(idx * 20, 0, 0)
    idx = idx + 1
    #  Add cube node
    scene.root_node.child_nodes.append(cube)
#  The path to the documents directory.
output = "out"  + "MeshGeometryData.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7400ASCII)

{{< /highlight >}}

Dans cet exemple, nous avons créé 3 nœuds cubes partagent le même maillage, chacun d'eux a un matériau différent avec des couleurs différentes.
