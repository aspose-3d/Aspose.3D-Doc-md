---
title: Créer un maillage et une scène 3D
type: docs
weight: 10
url: /fr/python-net/create-3d-mesh-and-scene/
description: Un maillage est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un maillage.
---
##  **Créer un maillage de cube 3D**
Un [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un maillage.

Afin de créer une surface Mesh, nous devons définir les points de contrôle et les polygones comme suit:

- [Définir les points de contrôle](/3d/fr/python-net/create-3d-mesh-and-scene/)
- [Créer des polygones avec PolygonBuilder Classe](/3d/fr/python-net/create-3d-mesh-and-scene/)
- [Créer des polygones](/3d/fr/python-net/create-3d-mesh-and-scene/)

Voici un exemple pour attacher un matériau Phong au nœud cube:
###  **Définir les points de contrôle**
Un maillage est composé d'un ensemble de points de contrôle dans l'espace et de polygones pour décrire la surface maillée, pour créer un maillage, nous devons définir les points de contrôle:

{{% alert color="primary" %}}

Les points de contrôle de toutes les géométries dans Aspose.3D utilisent la coordonnée homogène, donc c'est `Vector4` au lieu de `Vector3` dans l'exemple de code.

{{% /alert %}}

**Exemple:**

{{< highlight "python" >}}
from aspose.threed.utilities import Vector4

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize control points
controlPoints = [Vector4(-5.0, 0.0, 5.0, 1.0), Vector4(5.0, 0.0, 5.0, 1.0), Vector4(5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 10.0, 5.0, 1.0), Vector4(-5.0, 0.0, -5.0, 1.0), Vector4(5.0, 0.0, -5.0, 1.0), Vector4(5.0, 10.0, -5.0, 1.0), Vector4(-5.0, 10.0, -5.0, 1.0)]

{{< /highlight >}}


###  **Créer des polygones**
Les points de contrôle ne sont pas rendables, pour rendre le cube visible, nous devons définir des polygones de chaque côté:

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
controlPoints = DefineControlPoints()
#  Initialize mesh object
mesh = Mesh()
#  Add control points to the mesh
mesh.control_points.extend(controlPoints)
#  Create polygons to mesh
#  Front face (Z+)
mesh.create_polygon([0, 1, 2, 3 ])
#  Right side (X+)
mesh.create_polygon([1, 5, 6, 2 ])
#  Back face (Z-)
mesh.create_polygon([5, 4, 7, 6 ])
#  Left side (X-)
mesh.create_polygon([4, 0, 3, 7 ])
#  Bottom face (Y-)
mesh.create_polygon([0, 4, 5, 1 ])
#  Top face (Y+)
mesh.create_polygon([3, 2, 6, 7 ])

{{< /highlight >}}


###  **Créer des polygones avec PolygonBuilder Classe**
Nous pouvons également définir polygone par sommets avec la classe `PolygonBuilder`:

{{< highlight "python" >}}
from aspose.threed.entities import Mesh, PolygonBuilder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
controlPoints = DefineControlPoints()
#  Initialize mesh object
mesh = Mesh()
#  Add control points to the mesh
mesh.control_points.extend(controlPoints)
#  Indices of the vertices per each polygon
indices = [    0, 1, 2, 3,     1, 5, 6, 2,     5, 4, 7, 6,     4, 0, 3, 7,     0, 4, 5, 1,     3, 2, 6, 7 // Top face (Y+)
]
vertexId = 0
builder = PolygonBuilder(mesh)
for face in range(6):
    #  Start defining a new polygon
    builder.begin()
    for v in range(4):
        #  The indice of vertice per each polygon
        builder.add_vertex(indices[vertexId])
        vertexId = vertexId + 1
    #  Finished one polygon
    builder.end()

{{< /highlight >}}

Maintenant, c'est fini, pour rendre le maillage visible, nous devons préparer un nœud pour cela.
##  **Comment trianguler un maillage**
Le maillage triangulé est utile pour l'industrie du jeu car le triangulaire est la seule primitive prise en charge par le matériel GPU (les données non triangulaires sont triangulées au niveau du pilote, ce qui est inefficace en temps réel)

{{% alert color="primary" %}}

Dans cette version, nous avons seulement triangulé les polygones car il est requis par l'exportation de fichiers 3ds, les normes/uvs et autres éléments de sommet sont perdus au cours de cette procédure, nous pouvons l'implémenter à l'avenir.

{{% /alert %}}

Dans cet exemple, nous triangulons un Mesh en important un fichier FBX et le sauvegardons au format FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **Créer une scène de cube 3D**
Cette rubrique montre comment ajouter une géométrie de maillage à la scène 3D. L'exemple de code place un cube et enregistre la scène 3D dans les formats de fichier pris en charge.
###  **Créer un nœud cube**
Un nœud est invisible, mais la géométrie attachée au nœud peut être rendue.

{{% alert color="primary" %}}

L'objet de classe Mesh est utilisé dans le code. Nous pouvons [Créer un objet de classe `Mesh` comme raconté là](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Exemple**

{{< highlight "python" >}}
from aspose.threed import FileFormat, Node, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize scene object
scene = Scene()
#  Initialize Node class object
cubeNode = Node("cube")
#  Call Common class create mesh using polygon builder method to set mesh instance
mesh = Common.CreateMeshUsingPolygonBuilder()
#  Point node to the Mesh geometry
cubeNode.entity = mesh
#  Add Node to a scene
scene.root_node.child_nodes.append(cubeNode)
#  The path to the documents directory.
output = "out"  + "CubeScene.fbx"
#  Save 3D scene in the supported file formats
scene.save(output, FileFormat.FBX7400ASCII)

{{< /highlight >}}

{{% alert color="primary" %}}

REMARQUE: Les entités attachées au nœud racine sont généralement ignorées dans les logiciels CAD/CAM, nous devons donc créer un nouveau nœud pour rendre la géométrie.

{{% /alert %}}
