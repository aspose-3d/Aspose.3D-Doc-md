---
title: Exponera Geometrisk Transformation
type: docs
weight: 50
url: "/sv/nodejs-java/expose-geometric-transformation/"
description: "Aspose.3D för Node.js via Java möjliggör exponering av geometrisk transformation av en 3D-scen. Du kan utvärdera den globala transformationen med metoden evaluateGlobalTransform."
---

# **Exponera Geometrisk Transformation**
Aspose.3D för Node.js via Java tillåter exponering av geometrisk transformation av en 3D-scen. Du kan utvärdera den globala transformationen med `evaluateGlobalTransform`-metoden. Följande kodsnutt visar hur man exponerar den geometriska transformationen.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisera scenobjekt
var scene = new aspose.threed.Scene();

// Initialisera cylinder
var cylinder =new aspose.threed.Cylinder();

// Skapa ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Hämta Geometrisk Translation
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// Den första Console.WriteLine kommer att skriva ut transformationsmatrisen som inkluderar den geometriska transformationen
// medan den andra inte kommer att göra det.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}