---
title: Aspose.3D för Python via .NET 22,7 Utgivning
type: docs
weight: 6
url: /sv/python-net/aspose-3d-for-python-net-22-7-release-notes/
description: Utgivningsnoterna av Aspose.3D för Python via .NET 22,7.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 22.7.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1166 |Byt till USDZ som HTML5: s standardinriktning|Ny funktion|
|THREEDPYTHON-17 |Mesh kontrollpunkter exponeras inte i Python-versionen|Förbättring|

## API ändringar ##


Det gamla formatet A3DW användes som HTML5s interna format, Nu är det föråldrat och ersatt av USDZ, som kan ge fler funktioner och extensibilitet.

Eftersom 22.7 kommer `aspose.threed.entities.Mesh` att ha en fastighet `control_points`, det kan användas för att manuellt definiera hörn av Mesh.

Provkod:

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




