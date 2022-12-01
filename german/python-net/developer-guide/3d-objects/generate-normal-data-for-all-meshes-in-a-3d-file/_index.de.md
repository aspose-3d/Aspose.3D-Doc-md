---
title: Generieren Sie normale Daten für alle Maschen in einer Datei 3D
type: docs
weight: 70
url: /de/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Mithilfe von Aspose.3D für Python via .NETkönnen Entwickler normale Daten für alle Netze in jedem 3D-Modell (ohne die normalen Daten) generieren.
---
{{% alert color="primary" %}}

Verwendung[Aspose.3D für Python via .NET](https://products.aspose.com/3d/python-net/)Entwickler können normale Daten für alle Netze in jedem 3D-Modell generieren (ohne die normalen Daten).

{{% /alert %}}
## **Generieren Sie normale Daten für alle Maschen in einer Datei 3DS**
Die `generate_normal`-Methode, die von der [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-Klasse verfügbar ist, kann verwendet werden, um normale Daten für alle Netze in einer 3DS-Datei zu generieren. Wenn das Element `VertexElementSmoothingGroup` im Netz definiert wurde, werden die generierten normalen Daten durch die `VertexElementSmoothingGroup` geglättet.
### **Programmier probe**
Dieses Code beispiel lädt eine 3DS-Datei, besucht alle Knoten und erstellt normale Daten für alle Netze.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
