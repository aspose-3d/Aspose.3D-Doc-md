---
title: Créer 3D Maille et scène
type: docs
weight: 10
url: /fr/net/create-3d-mesh-and-scene/
description: Un maillage est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un maillage.
---
## **Créer un maillage Cube 3D**
Un [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un `Mesh`.

Afin de créer une surface `Mesh`, nous devons définir les points de contrôle et les polygones comme suit:

- [Définir les points de contrôle](/3d/fr/net/create-3d-mesh-and-scene/)
- [Créer des polygones avec la classe PolygonBuilder](/3d/fr/net/create-3d-mesh-and-scene/)
- [Créer des polygones](/3d/fr/net/create-3d-mesh-and-scene/)

Voici un exemple pour attacher un matériau Phong au nœud cube:
### **Définir les points de contrôle**
Un maillage est composé d'un ensemble de points de contrôle dans l'espace et de polygones pour décrire la surface maillée, pour créer un maillage, nous devons définir les points de contrôle:

{{% alert color="primary" %}}

Les points de contrôle de toutes les géométries du Aspose.3D utilisent des coordonnées homogènes, donc c'est `Vector4` au lieu de Vector3 dans l'exemple de code.

{{% /alert %}}

**Exemple:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-DefineControlPoints.cs" >}}


### **Créer des polygones**
Les points de contrôle ne sont pas rendables, pour rendre le cube visible, nous devons définir des polygones de chaque côté:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.cs" >}}


### **Créer des polygones avec la classe PolygonBuilder**
Nous pouvons également définir le polygone par sommets avec la classe `PolygonBuilder`:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.cs" >}}

Maintenant, c'est fini, pour rendre le maillage visible, nous devons préparer un nœud pour cela.
## **Comment trianguler un maillage**
Le maillage triangulé est utile pour l'industrie du jeu car le triangulaire est la seule primitive prise en charge par le matériel GPU (les données non triangulaires sont triangulées au niveau du pilote, ce qui est inefficace en temps réel)

{{% alert color="primary" %}}

Dans cette version, nous avons seulement triangulé les polygones car il est requis par l'exportation de fichiers 3ds, les normes/uvs et autres éléments de sommet sont perdus au cours de cette procédure, nous pouvons l'implémenter à l'avenir.

{{% /alert %}}

Dans cet exemple, nous triangulons un Mesh en important le fichier FBX et nous l'avons enregistré au format FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.cs" >}}
## **Créer une scène de cube 3D**
Cette rubrique montre comment ajouter la géométrie Mesh à la scène 3D. L'exemple de code place un cube et enregistre la scène 3D dans les formats de fichier pris en charge.
### **Créer un nœud cube**
Un nœud est invisible, mais la géométrie attachée au nœud peut être rendue.

{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons[Créer un objet de classe Mesh tel que raconté là-bas](https://docs.aspose.com/3d/net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Exemple**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-CubeScene-CreateCubeScene.cs" >}}

{{% alert color="primary" %}}

REMARQUE: Les entités attachées au nœud racine sont généralement ignorées dans les logiciels CAD/CAM, nous devons donc créer un nouveau nœud pour rendre la géométrie.

{{% /alert %}}
