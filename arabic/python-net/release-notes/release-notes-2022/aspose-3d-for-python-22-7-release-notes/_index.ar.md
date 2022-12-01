---
title: Aspose.3D ل Python via .NET 22.7 Release Nأوتس
type: docs
weight: 6
url: /ar/python-net/aspose-3d-for-python-net-22-7-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D ل Python via .NET 22.7.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 22.7.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1166 |Witch الساحرة إلى USDZ كما HTML5 التنسيق الداخلي الافتراضي|New eature|
|THREEDPYTHON-17 |لا تتعرض نقاط التحكم في Mesh في إصدار python|حركة بلا حدود|

## API التغييرات ##


Tتم استخدام تنسيق A3DW القديم كشكل داخلي HTML5 ، والآن هو obsoleted واستبدالها USDZ ، والتي يمكن أن توفر المزيد من الميزات والتوسع.

Since 22.7 سيكون `aspose.threed.entities.Mesh` خاصية `control_points` ، ويمكن استخدامه لتحديد vertices من esh esh يدويا.

Sرمز وافرة:

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




