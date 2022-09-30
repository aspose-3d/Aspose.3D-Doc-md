---
title: Transformation zum Knoten hinzufügen
type: docs
weight: 30
url: /de/net/adding-transformation-to-the-node/
description: TSR (Translation/Skalierung/Rotation) werden am häufigsten im Szenario 3D verwendet. Wir haben eine Klasse Transform bereit gestellt, um auf diese in Aspose.3D zuzugreifen.
---
{{% alert color="primary" %}}

Aspose.3D for .NET bietet an, Objekte im Raum 3D zu drehen. Es gibt drei Möglichkeiten, die Drehung des Objekts im Raum 3D, Euler winkeln, Quaternion und Custom Matrix zu definieren. Alle werden von der Klasse [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) unterstützt.

{{% /alert %}}

TSR (Translation/Skalierung/Rotation) werden am häufigsten im Szenario 3D verwendet. Wir haben eine Klasse `Transform` bereit gestellt, um auf diese in Aspose.3D zuzugreifen. Affine Transformationen umfassen:

- Übersetzung
- Skalierung
- Rotation
- Scher kartierung
- Squeeze-Mapping

{{% alert color="primary" %}}

Das Klassen objekt [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) wird im Code verwendet. Wir können[Erstellen Sie ein Mesh-Klassen objekt, wie es dort erzählt wird](/3d/de/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Drehen Sie durch Quaternion**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
## **Drehen Sie durch Euler Winkel**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
## **Individuelle Transformation matrix**
Wir können Matrix auch direkt verwenden:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
