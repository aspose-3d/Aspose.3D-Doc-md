---
title: Ajouter une propriété d'animation et une caméra cible d'installation dans le document 3D
type: docs
weight: 10
url: /fr/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java prend en charge le rendu de scène animée. Cet article explique les conditions préalables pour déplacer un objet.
---
## **Ajouter une propriété Animation dans le document 3D**
Aspose.3D for Java prend en charge le rendu de scène animée. Cet article explique les conditions préalables pour déplacer un objet.
### **Déplacer la position du cube**
{{% alert color="primary" %}}

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons[Créer un objet de classe Mesh tel que raconté là-bas](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Et il doit aussi animer la propriété de traduction locale du nœud:[Ajout de la transformation au nœud](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

Dans Aspose.3D for Java API, l'instance d'animation est en fait une animation sur image clé qui s'anime sur les propriétés. Dans les propriétés animées de commande, vous avez besoin d'une instance `CurveMapping` qui mappe les composants d'une propriété à différentes courbes, par exemple, une propriété `Vector3` peut avoir 3 composants `X`/`Y`/`Z`, qui installera trois canaux au `CurveMapping`, chaque canal peut avoir un ensemble de `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **Configuration de la caméra cible dans le fichier 3D**
Aspose.3D for Java propose d'installer l'appareil photo cible dans le fichier 3D. Dans certains formats de fichiers, la lumière/caméra prend en charge la cible, ce qui permet à la lumière/caméra toujours face à un nœud spécifié, cela est utile dans l'animation.

{{% alert color="primary" %}}

Les classes `Scene`, `Camera`, `Node` et `Transform` sont utilisées dans le code. Afin d'enregistrer une méthode `Scene`, `Scene.save` est utilisée, il accepte un nom de fichier avec un chemin complet et un paramètre `FileFormat`.

{{% /alert %}}

Dans l'exemple ci-dessous, la cible et l'appareil photo est configuré dans le fichier 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
