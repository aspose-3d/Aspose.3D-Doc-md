---
title: Adición de transformación al nodo
type: docs
weight: 10
url: /es/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API tiene soporte para rotar objetos en el espacio 3D. Hay tres formas de definir la rotación del objeto en el espacio 3D, los ángulos de Euler, Quaternion y Custom Matrix, todos ellos son compatibles con la clase Transform.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte para rotar objetos en el espacio 3D. Hay tres formas de definir la rotación de un objeto en el espacio 3D, los ángulos de Euler, Quaternion y Custom Matrix, todos ellos son compatibles con la clase `Transform`.

{{% /alert %}} 

TSR (Traducción/Escala/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una clase `Transform` para acceder a estos en Aspose.3D Las transformaciones afín incluyen:

- Traducción
- Escala
- Rotación
- Mapeo de cizalla
- Mapeo de apretar

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
##  **Girar por el cuaternión**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
##  **Girar por ángulos de Euler**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
##  **Matriz de transformación personalizada**
También podemos utilizar la matriz directamente:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
