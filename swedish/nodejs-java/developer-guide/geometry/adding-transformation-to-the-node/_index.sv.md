---
title: Lägger till transformation till noden
type: docs
weight: 10
url: "/sv/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D för Node.js via Java API har stöd för att rotera objekt i 3D-rymden. Det finns tre sätt att definiera ett objekts rotation i 3D-rymden, Euler-vinklar, Quaternion och Anpassad Matris, alla stöds av Transform-klassen."
---

{{% alert color="primary" %}}

Aspose.3D för Node.js via Java API har stöd för att rotera objekt i 3D-rymden. Det finns tre sätt att definiera ett objekts rotation i 3D-rymden, Euler-vinklar, Quaternion och Anpassad Matris, alla stöds av klassen `Transform`.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) används oftast i 3D-scenarier, vi tillhandahåller en klass `Transform` för att få åtkomst till dessa i Aspose.3D Affina transformationer inkluderar:

- Translation
- Scaling
- Rotation
- Shear mapping
- Squeeze mapping

## **Rotera med Euler-vinklar**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisera scenobjekt
var scene = new aspose.threed.Scene();

// Initialisera cylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Skapa ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Euler-vinklar
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Ange translation
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Spara
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Anpassad Transformationsmatris**
Vi kan också använda Matris direkt:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisera scenobjekt
var scene = new aspose.threed.Scene();

// Initialisera cylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Skapa ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Ange anpassad translationmatris
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Spara
scene.save("TransformationToNode.obj");

{{< /highlight >}}