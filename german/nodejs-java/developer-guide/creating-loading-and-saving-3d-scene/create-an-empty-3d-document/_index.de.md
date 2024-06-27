---
title: Erstellen Sie ein leeres 3D-Dokument
type: docs
weight: 20
url: /de/nodejs-java/create-an-empty-3d-document/
description: Aspose.3D for Node.js via Java API unterstützt es, eine 3D-Szene von Grund auf neu zu erstellen und dann im unterstützten 3D-Format zu speichern.
---
##  **Erstellen Sie eine leere 3D-Szene und speichern Sie im unterstützten 3D-Format**
Aspose.3D for Node.js via Java API unterstützt es, eine 3D-Szene von Grund auf neu zu erstellen und dann im unterstützten 3D-Format zu speichern.
###  **Erstellen einer leeren 3D-Szene**
Bitte führen Sie diese Schritte aus, um eine 3D-Szene mit Aspose.3D for Node.js via Java API zu erstellen:

1. Erstellen Sie eine Instanz des**Szene**Klasse, die 3D Szene darstellt.
1. Erstellen Sie ein 3D-Dokument, indem Sie die**Sparen**Methode der**Szene**Klassen instanz.
####  **Erstellen einer leeren 3D-Szene: Samples programmieren**
{{< highlight "java" >}}

var file="document.fbx";

// Create an object of the Scene class
var scene = new aspose.threed.Scene();

// Save 3D scene document
scene.save(file);

{{< /highlight >}}




