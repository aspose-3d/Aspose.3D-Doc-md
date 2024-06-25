---
title: Adición de transformación al nodo
type: docs
weight: 30
url: /es/net/adding-transformation-to-the-node/
description: TSR (Traducción/Escalado/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una clase Transform para acceder a estos en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET ofrece rotar objetos en el espacio 3D. Hay tres formas de definir la rotación de objetos en el espacio 3D, ángulos de Euler, Quaternion y Custom Matrix, todos ellos son compatibles con la clase [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (Traducción/Escalado/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una clase `Transform` para acceder a estos en Aspose.3D. Las transformaciones afín incluyen:

- Traducción
- Escala
- Rotación
- Mapeo de cizalla
- Mapeo de apretar

{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Girar por el cuaternión**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
##  **Girar por ángulos de Euler**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
##  **Matriz de transformación personalizada**
También podemos utilizar la matriz directamente:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
