---
title: Ajouter une propriété d'animation et configurer la caméra cible dans le document 3D
type: docs
weight: 10
url: /fr/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java prend en charge le rendu des scènes animées. Cet article explique les conditions préalables pour déplacer un objet.
---
##  **Ajouter la propriété Animation dans le document 3D**
Aspose.3D for Java prend en charge le rendu des scènes animées. Cet article explique les conditions préalables pour déplacer un objet.
###  **Déplacer la position du cube**
{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) et il doit aussi animer la propriété de traduction locale du nœud: [Ajout de la transformation au nœud](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

Dans Aspose.3D for Java API, l'instance d'animation est en fait une animation d'image clé qui s'anime sur les propriétés. Pour animer les propriétés, vous avez besoin d'une instance `CurveMapping` qui mappe les composants d'une propriété à différentes courbes, par exemple, une propriété `Vector3` peut avoir 3 composants `X`/`Y`/`Z`, qui mettra en place trois canaux dans `CurveMapping`, chaque canal peut avoir un ensemble de `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **Configurer la caméra cible dans le fichier 3D**
Aspose.3D for Java propose de configurer la caméra cible dans le fichier 3D. Dans certains formats de fichiers, la lumière/caméra prend en charge la cible, ce qui permet à la lumière/caméra toujours face à un nœud spécifié, ce qui est utile dans l'animation.

{{% alert color="primary" %}}

Les classes `Scene`, `Camera`, `Node` et `Transform` sont utilisées dans le code. Pour enregistrer une méthode `Scene`, `Scene.save`, elle accepte un nom de fichier avec le chemin complet et le paramètre `FileFormat`.

{{% /alert %}}

Dans l'exemple ci-dessous, la cible et la caméra sont configurés dans le fichier 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
