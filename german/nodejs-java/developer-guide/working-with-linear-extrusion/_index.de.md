---
title: Lineare Extrusion
type: docs
weight: 80
url: "/de/nodejs-java/working-with-linear-extrusion/"
description: "Aspose.3D für Node.js über Java bietet die Klasse LinearExtrusion, die eine 2D-Form als Eingabe entgegennimmt und die Form in der 3. Dimension erweitert."
---

# **Lineare Extrusion durchführen**
Aspose.3D für Node.js über Java bietet die Klasse `LinearExtrusion`, die eine 2D-Form als Eingabe entgegennimmt und die Form in der 3. Dimension erweitert. Der folgende Codeausschnitt zeigt, wie eine lineare Extrusion durchgeführt wird:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisieren des Basiskörpers, der extrudiert werden soll
// Initialisieren des Basiskonturs, der extrudiert werden soll
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Durchführen einer linearen Extrusion, indem eine 2D-Form als Eingabe übergeben und die Form in der 3. Dimension erweitert wird
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Erstellen einer Szene
var scene = new aspose.threed.Scene();

// Erstellen eines untergeordneten Knotens, indem die Extrusion übergeben wird
scene.getRootNode().createChildNode(extrusion);

// 3D-Szene speichern
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Scheiben in linearer Extrusion**
Aspose.3D für Node.js über Java bietet die Methode `setSlices` der Klasse `LinearExtrusion`. Die Methode `setSlices` definiert die Anzahl der Zwischenpunkte entlang des Pfads der Extrusion. Der folgende Codeausschnitt zeigt, wie die Methode `setSlices` in einer linearen Extrusion verwendet wird:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisieren des Basiskörpers, der extrudiert werden soll
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Erstellen einer Szene
var scene = new aspose.threed.Scene();

// Erstellen eines linken Knotens
var left=scene.getRootNode().createChildNode();
// Erstellen eines rechten Knotens
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Das Parameter "Slices" definiert die Anzahl der Zwischenpunkte entlang des Pfads der Extrusion
// Durchführen einer linearen Extrusion am linken Knoten unter Verwendung der Eigenschaft "slices"
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Durchführen einer linearen Extrusion am rechten Knoten unter Verwendung der Eigenschaft "slices"
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// 3D-Szene speichern
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Zentrum in linearer Extrusion**
Aspose.3D für Node.js über Java bietet die Methode `setCenter` der Klasse `LinearExtrusion`. Wenn die Methode `setCenter` auf true gesetzt ist, liegt der Extrusionsbereich von -Höhe/2 bis Höhe/2, andernfalls liegt die Extrusion von 0 bis Höhe. Der folgende Codeausschnitt zeigt, wie die Methode `setCenter` in einer linearen Extrusion verwendet wird:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisieren des Basiskörpers, der extrudiert werden soll
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Erstellen einer Szene
var scene = new aspose.threed.Scene();

// Erstellen eines linken Knotens
var left=scene.getRootNode().createChildNode();
// Erstellen eines rechten Knotens
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Setzen einer Referenzebene
var box=new aspose.threed.Box(0.01, 3, 3);

// Wenn die Eigenschaft "Center" true ist, liegt der Extrusionsbereich von -Höhe/2 bis Höhe/2, andernfalls liegt die Extrusion von 0 bis Höhe
// Durchführen einer linearen Extrusion am linken Knoten unter Verwendung der Eigenschaften "center" und "slices"
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Durchführen einer linearen Extrusion am rechten Knoten unter Verwendung der Eigenschaften "center" und "slices"
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// 3D-Szene speichern
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Drehung in linearer Extrusion**
Aspose.3D für Node.js über Java bietet die Methode `setTwist` der Klasse `LinearExtrusion`. Die Methode `setTwist` steuert den Rotationsgrad während der Extrusion der Form. Der folgende Codeausschnitt zeigt, wie die Methode `setTwist` in einer linearen Extrusion verwendet wird:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisieren des Basiskörpers, der extrudiert werden soll
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Erstellen einer Szene
var scene = new aspose.threed.Scene();

// Erstellen eines linken Knotens
var left=scene.getRootNode().createChildNode();
// Erstellen eines rechten Knotens
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Das Parameter "Direction" definiert die Richtung der Extrusion.
// Durchführen einer linearen Extrusion am linken Knoten unter Verwendung der Eigenschaften "twist" und "slices"
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Durchführen einer linearen Extrusion am rechten Knoten unter Verwendung der Eigenschaften "twist", "twist offset" und "slices"
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// 3D-Szene speichern
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Richtung in linearer Extrusion**
Aspose.3D für Node.js über Java bietet die Methode `setDirection` der Klasse `LinearExtrusion`. Die Methode `setDirection` definiert die Richtung der Extrusion. Der folgende Codeausschnitt zeigt, wie die Methode `setDirection` in einer linearen Extrusion verwendet wird:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisieren des Basiskörpers, der extrudiert werden soll
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Erstellen einer Szene
var scene = new aspose.threed.Scene();

// Erstellen eines linken Knotens
var left=scene.getRootNode().createChildNode();
// Erstellen eines rechten Knotens
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Das Parameter "Direction" definiert die Richtung der Extrusion.
// Durchführen einer linearen Extrusion am linken Knoten unter Verwendung der Eigenschaften "twist" und "slices"
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Durchführen einer linearen Extrusion am rechten Knoten unter Verwendung der Eigenschaften "twist", "slices" und "direction"
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// 3D-Szene speichern
scene.save("DirectionInLinearExtrusion.obj");


{{< /highlight >}}