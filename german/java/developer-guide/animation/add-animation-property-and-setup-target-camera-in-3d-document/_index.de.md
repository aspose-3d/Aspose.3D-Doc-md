---
title: Hinzufügen von Animations eigenschaft und Setup-Ziel kamera in einem 3D-Dokument
type: docs
weight: 10
url: /de/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java unterstützt das Rendern animierter Szene. In diesem Artikel werden die Voraussetzungen zum Verschieben eines Objekts erläutert.
---
##  **Animation-Eigenschaft in 3D-Dokument hinzufügen**
Aspose.3D for Java unterstützt das Rendern animierter Szene. In diesem Artikel werden die Voraussetzungen zum Verschieben eines Objekts erläutert.
###  **Bewegen Sie die Position des Würfels**
{{% alert color="primary" %}}

Das `Mesh`-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) und es muss auch die lokale Übersetzungs eigenschaft des Knotens animieren: [Hinzufügen der Transformation zum Knoten](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API ist die Animations instanz eigentlich eine Key-Frame-Animation, die auf Eigenschaften animiert. Um Eigenschaften zu animieren, benötigen Sie eine `CurveMapping`-Instanz, die Komponenten einer Eigenschaft verschiedenen Kurven zuordnet. Beispiels weise kann eine `Vector3`-Eigenschaft 3 Komponenten `X`/`Y`/`Z` haben. Das wird drei Kanäle in `CurveMapping` einrichten, jeder Kanal kann einen Satz von `Curve` haben.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **Richten Sie die Ziel kamera in 3D-Datei ein**
Aspose.3D for Java bietet an, die Ziel kamera in 3D-Datei einzurichten. In einigen Dateiformaten unterstützt Licht/Kamera das Ziel, wodurch das Licht/die Kamera immer einem bestimmten Knoten zugewandt ist. Dies ist in der Animation nützlich.

{{% alert color="primary" %}}

Die Klassen `Scene`, `Camera`, `Node` und `Transform` werden im Code verwendet. Um eine `Scene`, `Scene.save` Methode zu speichern, wird ein Dateiname mit vollständigem Pfad und `FileFormat` Parameter akzeptiert.

{{% /alert %}}

Im folgenden Beispiel wird das Ziel und die Kamera in der 3D-Datei eingerichtet:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
