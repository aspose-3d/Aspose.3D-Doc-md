---
title: Ajouter une propriété d'animation et configurer la caméra cible dans le document 3D
type: docs
weight: 10
url: /fr/python-net/add-animation-property-and-setup-target-camera-in-3d-document/
description: Dans Aspose.3D, l'animation d'objet est en fait une animation d'image clé qui anime sur les propriétés. Pour animer les propriétés, vous avez besoin d'une instance de CurveMapping qui mappe les composants d'une propriété à des courbes différentes, par exemple, une propriété Vector3 peut avoir 3 composants X/Y/Z, qui va mettre en place trois canaux dans CurveMapping, chaque canal peut avoir un ensemble de courbes.
---
##  **Ajouter la propriété Animation dans le document 3D**
Aspose.3D for Python via .NET prend en charge le rendu de la scène animée. Cet article explique les conditions préalables pour déplacer un objet.
###  **Déplacer la position du cube**
{{% alert color="primary" %}}

L'objet de classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](/3d/fr/net/create-and-read-an-existing-3d-scene/) et il doit aussi animer la propriété de traduction locale du nœud: [Ajout de la transformation au nœud](/3d/fr/net/adding-transformation-to-the-node/).

{{% /alert %}}

Dans Aspose.3D, l'animation d'objet est en fait une animation d'image clé qui anime sur les propriétés. Pour animer les propriétés, vous avez besoin d'une instance `CurveMapping` qui mappe les composants d'une propriété à différentes courbes, par exemple, une propriété `Vector3` peut avoir 3 composants `X`/`Y`/`Z`, qui mettra en place trois canaux dans `CurveMapping`, chaque canal peut avoir un ensemble de `Curve`.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-PropertyToDocument-AddAnimationPropertyToDocument.py" >}}
##  **Configurer la caméra cible dans le fichier 3D**
Aspose.3D for Python via .NET propose de configurer la caméra cible dans le fichier 3D. Dans certains formats de fichiers, la lumière/caméra prend en charge la cible, ce qui permet à la lumière/caméra toujours face à un nœud spécifié, ce qui est utile dans l'animation.

{{% alert color="primary" %}}

Les classes [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) et [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) sont utilisées dans le code. Pour enregistrer une scène, la méthode [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) est utilisée, elle accepte un nom de fichier avec le chemin complet et le paramètre [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

Dans l'exemple ci-dessous, la cible et la caméra sont configurés dans le fichier 3D:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-SetupTargetAndCamera-SetupTargetAndCamera.py" >}}
