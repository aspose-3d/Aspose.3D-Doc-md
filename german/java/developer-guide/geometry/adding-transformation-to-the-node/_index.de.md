---
title: Transformation zum Knoten hinzufügen
type: docs
weight: 10
url: /de/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API hat Unterstützung, um Objekte im Raum 3D zu drehen. Es gibt drei Möglichkeiten, die Drehung des Objekts im Raum 3D, Euler winkeln, Quaternion und Custom Matrix zu definieren. Alle werden von der Klasse Transform unterstützt.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API hat Unterstützung, um Objekte im Raum 3D zu drehen. Es gibt drei Möglichkeiten, die Drehung des Objekts im Raum 3D, Euler winkeln, Quaternion und Custom Matrix zu definieren. Alle werden von der Klasse `Transform` unterstützt.

{{% /alert %}} 

TSR (Übersetzung/Skalierung/Rotation) werden am häufigsten im Szenario 3D verwendet. Wir haben eine Klasse `Transform` bereit gestellt, um auf diese in Aspose.3D zuzugreifen. Affine-Transformationen umfassen:

- Übersetzung
- Skalierung
- Rotation
- Scher kartierung
- Squeeze-Mapping

{{% alert color="primary" %}} 

Das Klassen objekt `Mesh` wird im Code verwendet. Wir können[Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Drehen Sie durch Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
## **Drehen Sie durch Euler Winkel**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
## **Individuelle Transformation matrix**
Wir können Matrix auch direkt verwenden:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
