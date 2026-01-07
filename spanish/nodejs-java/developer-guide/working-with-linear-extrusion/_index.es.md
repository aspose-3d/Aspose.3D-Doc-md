---
title: Trabajando con Extrusión Lineal
type: docs
weight: 80
url: "/es/nodejs-java/working-with-linear-extrusion/"
description: Aspose.3D para Node.js a través de Java ofrece la clase LinearExtrusion, que toma una forma 2D como entrada y extiende la forma en la tercera dimensión.
---

# **Realizando Extrusión Lineal**
Aspose.3D para Node.js vía Java ofrece la clase `LinearExtrusion`, que toma una forma 2D como entrada y extiende la forma en la tercera dimensión. El siguiente fragmento de código muestra cómo realizar una extrusión lineal:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar la forma base a ser extruida
// Inicializar el perfil base a ser extruida
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Realizar extrusión lineal pasando una forma 2D como entrada y extendiendo la forma en la tercera dimensión
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Crear una escena
var scene = new aspose.threed.Scene();

// Crear un nodo hijo pasando la extrusión
scene.getRootNode().createChildNode(extrusion);

// Guardar escena 3D
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Rebanadas en Extrusión Lineal**
Aspose.3D para Node.js vía Java ofrece el `setSlices()` método de la clase `LinearExtrusion`. El método setSlices() define el número de puntos intermedios a lo largo de la trayectoria de la extrusión. El siguiente fragmento de código muestra cómo usar el método setSlices() en una extrusión lineal:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar el perfil base a ser extruido
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crear una escena
var scene = new aspose.threed.Scene();

// Crear nodo izquierdo
var left=scene.getRootNode().createChildNode();
// Crear nodo derecho
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// El parámetro Slices define el número de puntos intermedios a lo largo de la trayectoria de la extrusión
// Realizar extrusión lineal en el nodo izquierdo usando la propiedad slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Realizar extrusión lineal en el nodo derecho usando la propiedad slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// Guardar escena 3D
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Centro en Extrusión Lineal**
Aspose.3D para Node.js vía Java ofrece el `setCenter()` método de la clase `LinearExtrusion`. Si el método setCenter() está configurado en verdadero, el rango de extrusión es de -Altura/2 a Altura/2, de lo contrario, la extrusión es de 0 a Altura. El siguiente fragmento de código muestra cómo usar el método setCenter() en una extrusión lineal:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar la forma base a ser extruida
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crear una escena
var scene = new aspose.threed.Scene();

// Crear nodo izquierdo
var left=scene.getRootNode().createChildNode();
// Crear nodo derecho
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Establecer plano de tierra como referencia
var box=new aspose.threed.Box(0.01, 3, 3);

// Si la propiedad Center es verdadera, el rango de extrusión es de -Altura/2 a Altura/2, de lo contrario la extrusión es de 0 a Altura
// Realizar extrusión lineal en el nodo izquierdo usando la propiedad center y slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Realizar extrusión lineal en el nodo derecho usando la propiedad center y slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// Guardar escena 3D
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Giro en Extrusión Lineal**
Aspose.3D para Node.js vía Java ofrece el `setTwist()` método de la clase `LinearExtrusion`. El método setTwist() maneja el grado de rotación mientras extruye la forma. El siguiente fragmento de código muestra cómo usar el método setTwist() en una extrusión lineal:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar la forma base a ser extruida
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crear una escena
var scene = new aspose.threed.Scene();

// Crear nodo izquierdo
var left=scene.getRootNode().createChildNode();
// Crear nodo derecho
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La propiedad Giro define el grado de rotación mientras extruye la forma.
// Realizar extrusión lineal en el nodo izquierdo usando la propiedad giro y slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Realizar extrusión lineal en el nodo derecho usando la propiedad giro, giro offset y slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Guardar escena 3D
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Offset de Giro en Extrusión Lineal**
Aspose.3D para Node.js vía Java ofrece el método `setTwistOffset()` de la clase `LinearExtrusion`. El método setTwistOffset() define el offset de la rotación mientras extruye la forma. El siguiente fragmento de código muestra cómo usar el método setTwistOffset() en una extrusión lineal:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar la forma base a ser extruida
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crear una escena
var scene = new aspose.threed.Scene();

// Crear nodo izquierdo
var left=scene.getRootNode().createChildNode();
// Crear nodo derecho
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La propiedad Giro define el grado de rotación mientras extruye la forma.
// Realizar extrusión lineal en el nodo izquierdo usando la propiedad giro y slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Realizar extrusión lineal en el nodo derecho usando la propiedad giro, giro offset y slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Guardar escena 3D
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Dirección en Extrusión Lineal**
Aspose.3D para Node.js vía Java ofrece el método `setDirection()` de la clase `LinearExtrusion`. El método setDirection() define la dirección de la extrusión. El siguiente fragmento de código muestra cómo usar el método setDirection() en una extrusión lineal:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar la forma base a ser extruida
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crear una escena
var scene = new aspose.threed.Scene();

// Crear nodo izquierdo
var left=scene.getRootNode().createChildNode();
// Crear nodo derecho
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La propiedad Dirección define la dirección de la extrusión.
// Realizar extrusión lineal en el nodo izquierdo usando la propiedad giro y slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Realizar extrusión lineal en el nodo derecho usando la propiedad giro, slices, y dirección
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// Guardar escena 3D
scene.save("DirectionInLinearExtrusion.obj");

{{< /highlight >}}