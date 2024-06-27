---
title: Ajout de la transformation au nœud
type: docs
weight: 30
url: /fr/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe Transform pour y accéder dans Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET propose de faire pivoter des objets dans un espace 3D. Il existe trois façons de définir la rotation de l'objet dans l'espace 3D, les angles d'Euler, le quaternion et la matrice personnalisée, toutes sont supportées par la classe [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

Les TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe `Transform` pour y accéder dans Aspose.3D. Les transformations affines comprennent:

- Traduction
- Mise à l'échelle
- Rotation
- Cartographie de cisaillement
- Cartographie à presser

{{% alert color="primary" %}}

L'objet de classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) est utilisé dans le code. Nous pouvons [Créer un objet de classe `Mesh` comme raconté là](/3d/fr/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Tourner par Quaternion**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
##  **Tourner par Euler Angles**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
##  **Matrice de transformation personnalisée**
Nous pouvons également utiliser Matrix directement:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
