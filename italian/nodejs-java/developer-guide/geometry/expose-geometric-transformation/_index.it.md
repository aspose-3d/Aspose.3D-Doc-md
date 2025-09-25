---
title: Esporre Trasformazione Geometrica
type: docs
weight: 50
url: "/it/nodejs-java/expose-geometric-transformation/"
description: Aspose.3D per Node.js via Java consente di esporre la trasformazione geometrica di una scena 3D. È possibile valutare la trasformazione globale utilizzando il metodo evaluateGlobalTransform.
---

# **Esponi la Trasformazione Geometrica**
Aspose.3D for Node.js via Java permette di esporre la trasformazione geometrica di una scena 3D. Puoi valutare la trasformazione globale usando il metodo `evaluateGlobalTransform`. Il seguente frammento di codice mostra come esporre la trasformazione geometrica.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inizializza oggetto scena
var scene = new aspose.threed.Scene();

// Inizializza cilindro
var cylinder =new aspose.threed.Cylinder();

// Crea ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Ottieni Traslazione Geometrica
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// Il primo Console.WriteLine stamperà la matrice di trasformazione che include la trasformazione geometrica
// mentre il secondo non lo farà.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}