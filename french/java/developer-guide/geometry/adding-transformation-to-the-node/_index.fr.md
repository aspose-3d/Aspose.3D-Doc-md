---
title: Ajout de la transformation au nœud
type: docs
weight: 10
url: /fr/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API a un support pour faire tourner les objets dans l'espace 3D. Il existe trois façons de définir la rotation de l'objet dans l'espace 3D, les angles Euler, le Quaternion et la matrice personnalisée, toutes sont prises en charge par la classe Transform.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API a un support pour faire tourner les objets dans l'espace 3D. Il existe trois façons de définir la rotation de l'objet dans l'espace 3D, les angles Euler, le Quaternion et la matrice personnalisée, toutes sont prises en charge par la classe `Transform`.

{{% /alert %}} 

Les TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe `Transform` pour y accéder dans Aspose.3D Les transformations affines comprennent:

- Traduction
- Mise à l'échelle
- Rotation
- Cartographie de cisaillement
- Cartographie à presser

{{% alert color="primary" %}} 

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons[Créer un objet de classe Mesh tel que raconté là-bas](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Tourner par Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
## **Tourner par Euler Angles**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
## **Matrice de transformation personnalisée**
Nous pouvons également utiliser Matrix directement:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
