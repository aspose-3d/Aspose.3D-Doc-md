---
title: Working مع oointCبصوت عال
type: docs
weight: 150
url: /ar/python-net/working-with-pointcloud/
description: يسمح Aspose.3D for Python via .NET بفك تشفير شبكة من ملف Draco مباشرةً دون إنشاء مشهد باستخدام طريقة فك شفرة فئة DracoFormat.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.7 أو أكبر.

{{% /alert %}} 
#  **Dإيكودي إيش**
يسمح Aspose.3D for Python via .NET بفك تشفير شبكة من ملف Draco مباشرةً دون إنشاء مشهد باستخدام طريقة [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) لفئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "python" >}}
from aspose import pycore
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
pointCloud = pycore.cast(PointCloud, FileFormat.DRACO.decode("data-dir"  + "point_cloud_no_qp.drc"))

{{< /highlight >}}
#  **Encode esh sh**
يسمح Aspose.3D for Python via .NET بتشفير شبكة كروية إلى ملف Draco مباشرةً دون إنشاء مشهد باستخدام طريقة [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) لفئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")

{{< /highlight >}}
#  **Encode Sphere كما PointCبصوت عال**
يسمح Aspose.3D for Python via .NET بتشفير شبكة كروية إلى ملف Draco كسحابة نقاط باستخدام طريقة [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) لفئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoSaveOptions

options = DracoSaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc", options)

{{< /highlight >}}
#  **ترميز شبكة إلى PLY**
يسمح Aspose.3D for Python via .NET بتشفير شبكة إلى ملف PLY مباشرةً دون إنشاء مشهد باستخدام طريقة [Encode](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) لفئة [PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **شبكة فك شفرة من PLY**
يسمح Aspose.3D for Python via .NET بفك تشفير سحابة شبكية/نقاط من ملف PLY باستخدام طريقة [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) لفئة [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **تصدير إلى PLY مثل pottcloud**
يسمح Aspose.3D for Python via .NET بتصدير مشهد إلى PLY كنمط PointCloud باستخدام طريقة [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) لفئة [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import PlySaveOptions

options = PlySaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "data-dir"  + "sphere.ply", options)

{{< /highlight >}}
#  **تصدير مشهد 3D كسحابة نقطة**
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.8 أو أكبر.

{{% /alert %}} 

يسمح Aspose.3D for Python via .NET بتصدير مشهد 3D مثل potcloud باستخدام خاصية [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) من فئة [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import ObjSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
scene = Scene(Sphere())
options = ObjSaveOptions()
options.point_cloud = true 
scene.save("data-dir"  + "Export3DSceneAsPointCloud.obj", options)

{{< /highlight >}}
