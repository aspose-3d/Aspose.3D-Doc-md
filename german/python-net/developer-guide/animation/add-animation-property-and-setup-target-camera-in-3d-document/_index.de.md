﻿---
title: Hinzufügen von Animations eigenschaft und Setup-Ziel kamera im Dokument 3D
type: docs
weight: 10
url: /de/python-net/add-animation-property-and-setup-target-camera-in-3d-document/
description: In Aspose.3D ist Objekt animation tatsächlich eine Key-Frame-Animation, die auf Eigenschaften animiert. Um Eigenschaften zu animieren, benötigen Sie eine CurveMapping-Instanz, die Komponenten einer Eigenschaft verschiedenen Kurven zuordnet. Beispiels weise kann eine Vector3-Eigenschaft 3 Komponenten X/Y/Z enthalten, wodurch drei Kanäle in Curve Mapping eingerichtet werden. Jeder Kanal kann einen Satz haben von Kurven.
---
## **Animation-Eigenschaft im Dokument 3D hinzufügen**
Aspose.3D für Python via .NET unterstützt das Rendern animierter Szene. In diesem Artikel werden die Voraussetzungen zum Verschieben eines Objekts erläutert.
### **Bewegen Sie die Position des Würfels**
{{% alert color="primary" %}}

Das Klassen objekt [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) wird im Code verwendet. Wir können[Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](/3d/de/net/create-and-read-an-existing-3d-scene/)Und es muss auch die lokale Übersetzungs eigenschaft des Knotens animieren:[Hinzufügen der Transformation zum Knoten](/3d/de/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D ist Objekt animation tatsächlich eine Key-Frame-Animation, die auf Eigenschaften animiert. Um Eigenschaften zu animieren, benötigen Sie eine `CurveMapping`-Instanz, die Komponenten einer Eigenschaft verschiedenen Kurven zuordnet. Beispiels weise kann eine `Vector3`-Eigenschaft 3 Komponenten haben, die drei Kanäle in `CurveMapping` einrichten. Jeder Kanal kann einen Satz von `Curve` haben.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-PropertyToDocument-AddAnimationPropertyToDocument.py" >}}
## **Richten Sie die Ziel kamera in der Datei 3D ein**
Aspose.3D für Python via .NET bietet die Einrichtung der Ziel kamera in der Datei 3D. In einigen Dateiformaten unterstützt Licht/Kamera das Ziel, wodurch das Licht/die Kamera immer einem bestimmten Knoten zugewandt ist. Dies ist in der Animation nützlich.

{{% alert color="primary" %}}

Die Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) und [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) werden im Code verwendet. Um eine Szene zu speichern, wird die Methode [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) verwendet. Sie akzeptiert einen Dateinamen mit vollständigem Pfad und dem Parameter [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

Im folgenden Beispiel wird das Ziel und die Kamera in der Datei 3D eingerichtet:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-SetupTargetAndCamera-SetupTargetAndCamera.py" >}}
