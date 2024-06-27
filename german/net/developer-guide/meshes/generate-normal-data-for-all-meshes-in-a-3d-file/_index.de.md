---
title: Generieren Sie normale Daten für alle Maschen in einer 3D-Datei
type: docs
weight: 17
url: /de/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Mit Aspose.3D for .NET können Entwickler normale Daten für alle Maschen in jedem 3D-Modell generieren (ohne die normalen Daten).
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler normale Daten für alle Netze in jedem 3D-Modell generieren (ohne die normalen Daten).

{{% /alert %}}
##  **Generieren Sie normale Daten für alle Maschen in einer 3DS-Datei**
Die `GenerateNormal`-Methode, die von der [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-Klasse angezeigt wird, kann verwendet werden, um normale Daten für alle Netze in einer 3DS-Datei zu generieren. Wenn das `VertexElementSmoothingGroup`-Element im Netz definiert wurde, werden die generierten normalen Daten durch die `VertexElementSmoothingGroup` geglättet.
###  **Programmier probe**
Dieses Code beispiel lädt eine 3DS-Datei, besucht alle Knoten und erstellt normale Daten für alle Netze.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.cs" >}}
