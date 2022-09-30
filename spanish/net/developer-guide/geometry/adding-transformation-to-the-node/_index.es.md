---
title: Adición de transformación al nodo
type: docs
weight: 30
url: /es/net/adding-transformation-to-the-node/
description: TSR (Traducción/Escala/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una transformación de clase para acceder a ellos en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET ofrece rotar objetos en el espacio 3D. Hay tres formas de definir la rotación de objetos en el espacio 3D, ángulos Euler, Quaternion y Custom Matrix, todas ellas son compatibles con la clase [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (Traducción/Escala/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una clase `Transform` para acceder a ellos en Aspose.3D. Las transformaciones afines incluyen:

- Traducción
- Escalada
- Rotación
- Mapeo de cizalla
- Mapeo de apretar

{{% alert color="primary" %}}

El objeto de clase [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) se está utilizando en el código. Podemos[Crear un objeto de clase Mesh como se narra allí](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Girar por el cuaternión**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
## **Girar por ángulos de Euler**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
## **Matriz de transformación personalizada**
También podemos utilizar la matriz directamente:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
