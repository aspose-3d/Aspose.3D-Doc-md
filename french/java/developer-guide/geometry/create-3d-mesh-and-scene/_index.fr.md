---
title: Créer un maillage et une scène 3D
type: docs
weight: 40
url: /fr/java/create-3d-mesh-and-scene/
description: Un maillage est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un maillage.
---
##  **Créer un maillage de cube 3D**
Un `Mesh` est défini par un ensemble de points de contrôle et les nombreux polygones à n côtés selon les besoins. Cet article explique comment définir un `Mesh`.

Pour créer une surface `Mesh`, nous devons définir les points de contrôle et les polygones comme suit:

- [Définir les points de contrôle](/3d/fr/java/create-3d-mesh-and-scene-html/)
- [Créer des polygones avec PolygonBuilder Classe](/3d/fr/java/create-3d-mesh-and-scene-html/)
- [Créer des polygones](/3d/fr/java/create-3d-mesh-and-scene-html/)

Voici un exemple pour attacher un matériau Phong au nœud cube:
###  **Définir les points de contrôle**
Un maillage est composé d'un ensemble de points de contrôle dans l'espace et de polygones pour décrire la surface maillée, pour créer un maillage, nous devons définir les points de contrôle:

{{% alert color="primary" %}} 

Les points de contrôle de toutes les géométries dans Aspose.3D utilisent la coordonnée homogène, donc c'est `Vector4` au lieu de `Vector3` dans l'exemple de code.

{{% /alert %}} 

**Exemple:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



###  **Créer des polygones**
Les points de contrôle ne sont pas rendables, pour rendre le cube visible, nous devons définir des polygones de chaque côté:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



###  **Créer des polygones avec PolygonBuilder Classe**
Nous pouvons également définir polygone par sommets avec la classe PolygonBuilder:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Maintenant, c'est fini, pour rendre le maillage visible, nous devons préparer un nœud pour cela.
##  **Comment trianguler un maillage**
Le maillage triangulé est utile pour l'industrie du jeu car le triangulaire est la seule primitive prise en charge par le matériel GPU (les données non triangulaires sont triangulées au niveau du pilote, ce qui est inefficace en temps réel)

{{% alert color="primary" %}} 

Dans cette version, nous avons seulement triangulé les polygones car il est requis par l'exportation de fichiers 3ds, les normes/uvs et autres éléments de sommet sont perdus au cours de cette procédure, nous pouvons l'implémenter à l'avenir.

{{% /alert %}} 

Dans cet exemple, nous triangulons un Mesh en important un fichier FBX et le sauvegardons au format FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
##  **Créer une scène de cube 3D**
Cette rubrique montre comment ajouter une géométrie de maillage à la scène 3D. L'exemple de code place un cube et enregistre la scène 3D dans les formats de fichier pris en charge.
###  **Créer un nœud cube**
Un nœud est invisible, mais la géométrie attachée au nœud peut être rendue.

{{% alert color="primary" %}} 

L'objet de classe Mesh est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Exemple:**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

REMARQUE: Les entités attachées au nœud racine sont généralement ignorées dans les logiciels CAD/CAM, nous devons donc créer un nouveau nœud pour rendre la géométrie.

{{% /alert %}}
