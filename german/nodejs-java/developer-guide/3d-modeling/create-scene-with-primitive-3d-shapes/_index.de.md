---
title: "Szene mit primitiven 3D-Formen erstellen"
type: docs
weight: 20
url: "/de/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: "Aspose.3D für Node.js über die Java API unterstützt primitive 3D-Formen. Alle parametrisierten Primitive werden beim Speichern in jedem unterstützten Ausgabedateiformat automatisch in ein Mesh konvertiert."
---

{{% alert color="primary" %}} 

Aspose.3D for Node.js via Java API hat Unterstützung für primitive 3D-Formen. Alle parametrisierten Primitive werden beim Speichern in jedem unterstützten Ausgabeformat automatisch in ein Mesh konvertiert.

{{% /alert %}} 
## **Szene aus primitiven 3D-Formen erstellen**
Das Modellieren ist ein Prozess der reinen Erschaffung, und die Aspose.3D API unterstützt das Erstellen einer Szene mit primitiven 3D-Formen.
### **Programmierbeispiel**
Dieses Codebeispiel erstellt eine Szene mit primitiven 3D-Formen und speichert sie in der OBJ-Datei.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisiere eine 3D-Szene
var scene = new aspose.threed.Scene();

// Erstelle einen Box-Modell
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Erstelle einen Zylinder-Modell
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Speichere Zeichnung im OBJ-Format
scene.save("test.obj");


{{< /highlight >}}