---
title: Forma primitiva a malla
type: docs
weight: 20
url: "/es/nodejs-java/primitive-shape-to-mesh/"
description: Aspose.3D para Node.js a través de la API de Java tiene soporte para convertir cualquier forma primitiva en malla. Las formas primitivas incluyen los objetos más básicos y utilizados como caja, esfera, plano, cilindro y toro.
---

## **Convertir Forma Primitiva a Malla**
Aspose.3D para Node.js a través de la API de Java tiene soporte para convertir cualquier forma primitiva a malla. Las formas primitivas incluyen los objetos más básicos y utilizados como caja, esfera, plano, cilindro y toro.

{{% alert color="primary" %}}

Cualquier clase que implemente la interfaz IMeshConvertible se puede convertir a malla al exportar a cualquier formato de archivo 3D.

{{% /alert %}}
### **Convertir Primitiva Esfera a Malla**
Una esfera es un objeto geométrico perfectamente redondo en el espacio tridimensional que aparece desde balones deportivos hasta planetas en el espacio. Usemos la primitiva Esfera para crear una malla.
El ejemplo de código a continuación convierte una Esfera a malla.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar objeto por clase Esfera
var convertible = new aspose.threed.Sphere();

// Convertir una Esfera a Malla
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir Caja a Malla**
Una Caja describe una variedad de contenedores y receptáculos para uso permanente como almacenamiento, o para uso temporal, a menudo para transportar contenidos. Usemos la primitiva Caja para crear una malla. El ejemplo de código a continuación convierte una Caja a malla.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar objeto por clase Caja
var convertible = new aspose.threed.Box();

// Convertir una Caja a Malla
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir un Plano a Malla**
Un plano se extiende infinitamente sin grosor. Un ejemplo de un plano es un plano de coordenadas. Usemos la primitiva Plano para crear una malla. El ejemplo de código a continuación convierte un Plano a malla.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar objeto por clase Plano
var convertible = new aspose.threed.Plane();

// Convertir un Plano a Malla
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir un Cilindro a Malla**
Un cilindro es una de las formas geométricas curvilíneas más básicas, la superficie formada por los puntos a una distancia fija de una línea recta dada, el eje del cilindro. Se puede utilizar en muchos lugares, por ejemplo como un pilar frente a una casa o como un eje de transmisión de un automóvil. Usemos la primitiva Cilindro para crear una malla. El ejemplo de código a continuación convierte un Cilindro a malla.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar objeto por clase Cilindro
var convertible = new aspose.threed.Cylinder();

// Convertir un Cilindro a Malla
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir un Toro a Malla**
Un toro es una superficie de revolución generada al hacer girar un círculo en el espacio tridimensional alrededor de un eje coplanario con el círculo. Si el eje de revolución no toca el círculo, la superficie tiene forma de anillo y se llama toro de revolución. Usemos la primitiva Toro para crear una malla. El ejemplo de código a continuación convierte un Toro a malla.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inicializar objeto por clase Toro
var convertible = new aspose.threed.Torus();

// Convertir un Toro a Malla
var mesh = convertible.toMesh();

{{< /highlight >}}