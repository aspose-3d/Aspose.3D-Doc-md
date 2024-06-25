---
title: Transformation zum Knoten hinzufügen
type: docs
weight: 10
url: /de/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API bietet Unterstützung für das Drehen von Objekten in 3D Raum. Es gibt drei Möglichkeiten, die Rotation des Objekts im Raum 3D zu definieren, Euler winkel, Quaternion und Custom Matrix. Alle werden von der Klasse Transform unterstützt.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API bietet Unterstützung für das Drehen von Objekten in 3D Raum. Es gibt drei Möglichkeiten, die Rotation des Objekts im Raum 3D zu definieren, Euler winkel, Quaternion und Custom Matrix. Alle werden von der `Transform`-Klasse unterstützt.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class `Transform` to access these in Aspose.3D Affine transformations include:

- Übersetzung
- Skalierung
- Rotation
- Scher kartierung
- Squeeze-Mapping

{{% alert color="primary" %}} 

Das `Mesh`-Klassen objekt wird im Code verwendet. Wir können [Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
##  **Drehen Sie durch Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
##  **Drehen Sie durch Euler Winkel**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
##  **Individuelle Transformation matrix**
Wir können Matrix auch direkt verwenden:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
