---
title: Aggiunta della trasformazione al nodo
type: docs
weight: 10
url: /it/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API supporta la rotazione degli oggetti nello spazio 3D. Esistono tre modi per definire la rotazione dell'oggetto nello spazio 3D, angoli di Eulero, Quaternion e Custom Matrix, tutti supportati dalla classe Transform.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporta la rotazione degli oggetti nello spazio 3D. Esistono tre modi per definire la rotazione dell'oggetto nello spazio 3D, angoli di Eulero, Quaternion e Custom Matrix, tutti supportati dalla classe `Transform`.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe `Transform` per accedere a questi in Aspose.3D Le trasformazioni affini includono:

- Traduzione
- Scalatura
- Rotazione
- Mappatura del taglio
- Spremi la mappatura

{{% alert color="primary" %}} 

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
##  **Ruota da Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
##  **Ruota per angoli di Eulero**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
##  **Matrice di trasformazione personalizzata**
Possiamo anche usare Matrix direttamente:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
