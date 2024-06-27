---
title: Fügen Sie Knoten hierarchie hinzu und teilen Sie geometrische Daten von Mesh unter mehreren Knoten der 3D-Szene
type: docs
weight: 20
url: /de/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java unterstützt den Aufbau einer Hierarchie von Knoten. Der Knoten ist ein grundlegender Baustein der 3D-Szene, und eine Knoten hierarchie definiert die logische Struktur der 3D-Szene und bietet sichtbaren Inhalt, indem Geometrien, Lichter und Kameras an Knoten angebracht werden.
---
##  **Knoten hierarchie in 3D Szenen dokument hinzufügen**
Aspose.3D for Java unterstützt den Aufbau einer Hierarchie von Knoten. Der `Node` ist ein grundlegender Baustein der 3D-Szene. Eine Knoten hierarchie definiert die logische Struktur der 3D-Szene und bietet sichtbaren Inhalt, indem Geometrien, Lichter und Kameras an Knoten angebracht werden.
###  **Szenen-Grafik-Beispiel**

In Aspose.3D kann jede `Node`-Instanz mehrere unter geordnete Knoten haben. In diesem Beispiel haben wir einen Knoten mit zwei Würfel knoten erstellt. Wenn wir den Stamm knoten drehen, sind auch alle unter geordneten Knoten betroffen:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
##  **Teilen Sie die Geometrie daten von Mesh zwischen mehreren Knoten**
Um den Speicher bedarf zu verringern, kann eine einzelne Instanz der `Mesh`-Klasse an verschiedene Instanzen der `Node`-Klasse gebunden werden. Stellen Sie sich vor, dass Sie ein System benötigen, in dem alle 3D Würfel nicht zu unterscheiden schienen, aber Sie benötigten zahlreiche viele davon. Sie können Speicher platz sparen, indem Sie ein Mesh-Objekt erstellen, wenn das System gestartet wird. Zu diesem Zeitpunkt erstellen Sie jedes Mal, wenn Sie eine andere Form benötigen, ein weiteres Knoten objekt und zeigen diesen Knoten auf das Knoten `Mesh`. Dies wird als Instancing bezeichnet. Aspose.3D for Java APIs erlauben Instancing.
###  **Instancing Beispiel**
In den RTS-Spielen (Echtzeit strategie) wie können wir immer mehrere NPCs (Non-Player Character) mit demselben 3D-Modell sehen, möglicher weise in verschiedenen Farben. Die Rendering-Engine teilt normaler weise dieselben Mesh-Geometrie-Daten über verschiedene NPCs hinweg wird Instancing genannt.

{{% alert color="primary" %}} 

Das `Mesh`-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Demonstration des Beispiel codes:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


In diesem Beispiel haben wir 3 Würfel knoten erstellt, die dasselbe Netz haben. Jeder von ihnen hat unterschied liches Material mit unterschied lichen Farben.
