---
title: Aspose.3D per Python via .NET Note di rilascio 22.7
type: docs
weight: 6
url: /it/python-net/aspose-3d-for-python-net-22-7-release-notes/
description: Le note di rilascio dello Aspose.3D per Python via .NET 22,7.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 22.7.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1166 |Passa allo USDZ come formato interno predefinito dello HTML5|Nuova funzione|
|THREEDPYTHON-17 |I punti di controllo di Mesh non sono esposti nella versione Python|Miglioramento|

## API modifiche ##


Il vecchio formato A3DW è stato utilizzato come formato interno dello HTML5, ora è obsoleto e sostituito dallo USDZ, che può fornire più funzionalità ed estensibilità.

Poiché 22,7 lo `aspose.threed.entities.Mesh` avrà una proprietà `control_points`, può essere utilizzato per definire manualmente i vertici della Mesh.

Codice del campione:

{{< highlight "python" >}}

from aspose.threed.entities import Mesh
from aspose.threed.utilities import Vector4

controlPoints = [
	Vector4( -5.0, 0.0, 5.0, 1.0),
	Vector4( 5.0, 0.0, 5.0, 1.0),
	Vector4( 5.0, 10.0, 5.0, 1.0),
	Vector4( -5.0, 10.0, 5.0, 1.0),
	Vector4( -5.0, 0.0, -5.0, 1.0),
	Vector4( 5.0, 0.0, -5.0, 1.0),
	Vector4( 5.0, 10.0, -5.0, 1.0),
	Vector4( -5.0, 10.0, -5.0, 1.0)
]# Initialize mesh object
mesh = Mesh();
# Add control points to the mesh
for pt in controlPoints:
	mesh.control_points.append(pt)
# Create polygons to mesh
# Front face (Z+)
mesh.create_polygon(0, 1, 2, 3);
# Right side (X+)
mesh.create_polygon(1, 5, 6, 2);
# Back face (Z-)
mesh.create_polygon(5, 4, 7, 6);
# Left side (X-)
mesh.create_polygon(4, 0, 3, 7);
# Bottom face (Y-)
mesh.create_polygon(0, 4, 5, 1);
# Top face (Y+)
mesh.create_polygon(3, 2, 6, 7);

{{< /highlight >}}




