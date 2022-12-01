---
title: Transformation zum Knoten hinzufügen
type: docs
weight: 30
url: /de/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Skalierung/Rotation) werden am häufigsten im Szenario 3D verwendet. Wir haben eine Klasse Transform bereit gestellt, um auf diese in Aspose.3D zuzugreifen.
---
{{% alert color="primary" %}}

Aspose.3D für Python via .NET bietet an, Objekte im Raum 3D zu drehen. Es gibt drei Möglichkeiten, die Drehung des Objekts im Raum 3D, Euler winkeln, Quaternion und Custom Matrix zu definieren. Alle werden von der Klasse [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) unterstützt.

{{% /alert %}}

TSR (Translation/Skalierung/Rotation) werden am häufigsten im Szenario 3D verwendet. Wir haben eine Klasse `Transform` bereit gestellt, um auf diese in Aspose.3D zuzugreifen. Affine Transformationen umfassen:

- Übersetzung
- Skalierung
- Rotation
- Scher kartierung
- Squeeze-Mapping

{{% alert color="primary" %}}

Das Klassen objekt [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) wird im Code verwendet. Wir können[Erstellen Sie ein `Mesh`-Klassenobjekt, wie es dort erzählt wird](/3d/de/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Drehen Sie durch Quaternion**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
## **Drehen Sie durch Euler Winkel**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
## **Individuelle Transformation matrix**
Wir können Matrix auch direkt verwenden:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
