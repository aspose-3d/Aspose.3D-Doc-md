---
title: Ajout de la transformation au nœud
type: docs
weight: 30
url: /fr/net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe Transform pour y accéder en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET propose de faire pivoter des objets dans l'espace 3D. Il existe trois façons de définir la rotation de l'objet dans l'espace 3D, les angles Euler, le Quaternion et la matrice personnalisée, toutes sont prises en charge par la classe [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe `Transform` pour y accéder en Aspose.3D. Les transformations affines comprennent:

- Traduction
- Mise à l'échelle
- Rotation
- Cartographie de cisaillement
- Cartographie à presser

{{% alert color="primary" %}}

L'objet de classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) est utilisé dans le code. Nous pouvons[Créer un objet de classe Mesh tel que raconté là-bas](/3d/fr/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Tourner par Quaternion**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
## **Tourner par Euler Angles**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
## **Matrice de transformation personnalisée**
Nous pouvons également utiliser Matrix directement:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
