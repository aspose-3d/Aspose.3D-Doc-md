---
title: Ajouter une propriété d'animation et configurer la caméra cible dans le document 3D
type: docs
weight: 10
url: /fr/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: Dans Aspose.3D, l'animation d'objet est en fait une animation d'image clé qui anime sur les propriétés. Pour animer les propriétés, vous avez besoin d'une instance de CurveMapping qui mappe les composants d'une propriété à des courbes différentes, par exemple, une propriété Vector3 peut avoir 3 composants X/Y/Z, qui va mettre en place trois canaux dans CurveMapping, chaque canal peut avoir un ensemble de courbes.
---
##  **Ajouter la propriété Animation dans le document 3D**
Aspose.3D for .NET prend en charge le rendu des scènes animées. Cet article explique les conditions préalables pour déplacer un objet.
###  **Déplacer la position du cube**
{{% alert color="primary" %}}

L'objet de classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](/3d/fr/net/create-and-read-an-existing-3d-scene/) et il doit aussi animer la propriété de traduction locale du nœud: [Ajout de la transformation au nœud](/3d/fr/net/adding-transformation-to-the-node/).

{{% /alert %}}

Dans Aspose.3D, l'animation d'objet est en fait une animation d'image clé qui anime sur les propriétés. Pour animer les propriétés, vous avez besoin d'une instance `CurveMapping` qui mappe les composants d'une propriété à différentes courbes, par exemple, une propriété `Vector3` peut avoir 3 composants `X`/`Y`/`Z`, qui mettra en place trois canaux dans `CurveMapping`, chaque canal peut avoir un ensemble de `Curve`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
##  **Configurer la caméra cible dans le fichier 3D**
Aspose.3D for .NET propose de configurer la caméra cible dans le fichier 3D. Dans certains formats de fichiers, la lumière/caméra prend en charge la cible, ce qui permet à la lumière/caméra toujours face à un nœud spécifié, ce qui est utile dans l'animation.

{{% alert color="primary" %}}

Les classes [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) et [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) sont utilisées dans le code. Pour enregistrer une méthode `Scene`, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) est utilisée, elle accepte un nom de fichier avec chemin complet et paramètre [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

Dans l'exemple ci-dessous, la cible et la caméra sont configurés dans le fichier 3D:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
