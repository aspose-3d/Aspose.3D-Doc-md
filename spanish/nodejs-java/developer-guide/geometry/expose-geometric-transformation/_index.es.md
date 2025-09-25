---
title: Exponer Transformación Geométrica
type: docs
weight: 50
url: "/es/nodejs-java/expose-geometric-transformation/"
description: Aspose.3D para Node.js a través de Java permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método evaluateGlobalTransform.
---

# **Exponer Transformación Geométrica**
Aspose.3D para Node.js vía Java permite exponer la transformación geométrica de una escena 3D. Puede evaluar la transformación global utilizando el método `evaluateGlobalTransform`. El siguiente fragmento de código muestra cómo exponer la transformación geométrica.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inicializar objeto de escena
var scene = new aspose.threed.Scene();

// Inicializar cilindro
var cylinder =new aspose.threed.Cylinder();

// Crear ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Obtener Traducción Geométrica
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// La primera Console.WriteLine mostrará la matriz de transformación que incluye la transformación geométrica
// mientras que la segunda no lo hará.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}