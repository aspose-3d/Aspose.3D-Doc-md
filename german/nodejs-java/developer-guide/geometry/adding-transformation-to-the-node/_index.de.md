---
title: Das Hinzufügen einer Transformation zum Knoten
type: docs
weight: 10
url: "/de/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D für Node.js über die Java API unterstützt die Rotation von Objekten im 3D-Raum. Es gibt drei Möglichkeiten, die Rotation eines Objekts im 3D-Raum zu definieren: Euler-Winkel, Quaternion und benutzerdefinierte Matrix, alle werden von der Klasse Transform unterstützt."
---

{{% alert color="primary" %}}

Aspose.3D für Node.js über die Java API unterstützt das Rotieren von Objekten im 3D-Raum. Es gibt drei Möglichkeiten, die Rotation eines Objekts im 3D-Raum zu definieren: Euler-Winkel, Quaternion und benutzerdefinierte Matrix, alle werden von der Klasse `Transform` unterstützt.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) werden am häufigsten in 3D-Szenarien verwendet, wir haben eine Klasse `Transform` bereitgestellt, um Zugriff auf diese in Aspose.3D-affinen Transformationen zu erhalten. Diese beinhalten:

- Translation
- Scaling
- Rotation
- Scherabbildung
- Quetschabbildung

## **Rotieren mit Euler-Winkeln**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisiere Szenenobjekt
var scene = new aspose.threed.Scene();

// Initialisiere Zylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Erstelle ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Euler-Winkel
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Setze Translation
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Speichern
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Benutzerdefinierte Transformationsmatrix**
Wir können auch direkt eine Matrix verwenden:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisiere Szenenobjekt
var scene = new aspose.threed.Scene();

// Initialisiere Zylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Erstelle ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Setze benutzerdefinierte Translationsmatrix
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Speichern
scene.save("TransformationToNode.obj");

{{< /highlight >}}