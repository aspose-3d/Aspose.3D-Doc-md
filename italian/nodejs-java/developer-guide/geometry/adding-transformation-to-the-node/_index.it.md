---
title: Aggiunta di una Trasformazione al Nodo
type: docs
weight: 10
url: "/it/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D per Node.js tramite API Java offre il supporto per ruotare gli oggetti nello spazio 3D. Esistono tre modi per definire la rotazione di un oggetto nello spazio 3D: angoli di Eulero, Quaternion e Matrice personalizzata, tutti supportati dalla classe Transform."
---

{{% alert color="primary" %}}

Aspose.3D for Node.js via Java API ha il supporto per ruotare oggetti nello spazio 3D. Ci sono tre modi per definire la rotazione di un oggetto nello spazio 3D, angoli di Eulero, Quaternion e Matrice Personalizzata, tutti supportati dalla classe `Transform`.

{{% /alert %}}

TSR (Traduzione/Scala/Rotazione) sono più comunemente usati in uno scenario 3D, abbiamo fornito una classe `Transform` per accedere a queste in Aspose.3D. Le trasformazioni affini includono:

- Traduzione
- Scala
- Rotazione
- Mappatura di taglio
- Mappatura di spremitura

## **Ruota con Angoli di Eulero**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inizializza oggetto scena
var scene = new aspose.threed.Scene();

// Inizializza cilindro
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Crea ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Angoli di Eulero
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Imposta la traduzione
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Salva
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Trasformazione Matriciale Personalizzata**
Possiamo anche usare direttamente una Matrice:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Inizializza oggetto scena
var scene = new aspose.threed.Scene();

// Inizializza cilindro
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Crea ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Imposta la matrice di traduzione personalizzata
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Salva
scene.save("TransformationToNode.obj");

{{< /highlight >}}
