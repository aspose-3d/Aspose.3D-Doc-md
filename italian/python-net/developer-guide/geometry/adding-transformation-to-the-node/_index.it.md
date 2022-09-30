---
title: Aggiunta della trasformazione al nodo
type: docs
weight: 30
url: /it/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe Transform per accedervi nello Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D per Python via .NET offre di ruotare gli oggetti nello spazio 3D. Esistono tre modi per definire la rotazione dell'oggetto nello spazio 3D, gli angoli di Eulero, Quaternion e Custom Matrix, tutti supportati dalla classe [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (Translation/Scaling/Rotation) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe `Transform` per accedervi nello Aspose.3D. Le trasformazioni affini includono:

- Traduzione
- Scalatura
- Rotazione
- Mappatura del taglio
- Spremi la mappatura

{{% alert color="primary" %}}

L'oggetto della classe [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) viene utilizzato nel codice. Possiamo[Creare un oggetto di classe `Mesh` come narrato lì](/3d/it/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Ruota da Quaternion**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
## **Ruota per angoli di Eulero**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
## **Matrice di trasformazione personalizzata**
Possiamo anche usare Matrix direttamente:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
