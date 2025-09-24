---
title: Agregando Transformación al Nodo
type: docs
weight: 10
url: "/es/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D para Node.js a través de la API de Java tiene soporte para rotar objetos en el espacio 3D. Hay tres formas de definir la rotación de un objeto en el espacio 3D: ángulos de Euler, Quaternion y Matriz Personalizada, todas ellas son compatibles con la clase Transform."
---

{{% alert color="primary" %}}

Aspose.3D para Node.js a través de la API de Java tiene soporte para rotar objetos en el espacio 3D. Hay tres formas de definir la rotación de un objeto en el espacio 3D, ángulos de Euler, Quaternion y Matriz Personalizada, todas ellas son compatibles con la clase `Transform`.

{{% /alert %}}

TSR (Traslación/Escalado/Rotación) se utilizan más comúnmente en escenarios 3D, proporcionamos una clase `Transform` para acceder a estas en Aspose.3D. Las transformaciones afines incluyen:

- Traslación
- Escalado
- Rotación
- Mapeo de cizallamiento
- Mapeo de estiramiento

## **Rotar por Ángulos de Euler**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inicializar objeto de escena
var scene = new aspose.threed.Scene();

// Inicializar cilindro
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Crear ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Ángulos de Euler
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Establecer traslación
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Guardar
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Matriz de Transformación Personalizada**
También podemos usar Matrix directamente:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inicializar objeto de escena
var scene = new aspose.threed.Scene();

// Inicializar cilindro
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Crear ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Establecer matriz de traslación personalizada
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Guardar
scene.save("TransformationToNode.obj");

{{< /highlight >}}
