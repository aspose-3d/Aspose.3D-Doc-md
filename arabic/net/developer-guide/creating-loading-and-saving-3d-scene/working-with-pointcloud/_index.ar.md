---
title: Working مع oointCبصوت عال
type: docs
weight: 150
url: /ar/net/working-with-pointcloud/
description: Aspose.3D for .NET يسمح بفك تشفير شبكة من ملف Draco مباشرةً دون إنشاء مشهد باستخدام طريقة فك تشفير فئة dracofformat.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.7 أو أكبر.

{{% /alert %}} 
#  **Dإيكودي إيش**
Aspose.3D for .NET يسمح بفك تشفير شبكة من ملف Draco مباشرةً دون إنشاء مشهد باستخدام طريقة [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) لفئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var pointCloud = (PointCloud)FileFormat.Draco.Decode("point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Encode esh sh**
Aspose.3D for .NET يسمح بتشفير شبكة كروية إلى ملف Draco مباشرةً دون إنشاء مشهد باستخدام طريقة [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) لفئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
#  **Encode Sphere كما PointCبصوت عال**
Aspose.3D for .NET يسمح بتشفير شبكة كروية إلى ملف Draco كسحابة نقطة باستخدام طريقة [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) لفئة [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() { PointCloud = true });

{{< /highlight >}}
#  **ترميز شبكة إلى PLY**
Aspose.3D for .NET يسمح بتشفير شبكة إلى ملف PLY مباشرةً دون إنشاء مشهد باستخدام طريقة [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) لفئة [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **شبكة فك شفرة من PLY**
Aspose.3D for .NET يسمح بفك تشفير سحابة شبكية/نقاط من ملف PLY باستخدام طريقة [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) لفئة [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **تصدير إلى PLY مثل pottcloud**
Aspose.3D for .NET يسمح بتصدير مشهد إلى PLY مثل potcloud باستخدام طريقة [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) لفئة [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions() { PointCloud = true });


{{< /highlight >}}
#  **تصدير مشهد 3D كسحابة نقطة**
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.8 أو أكبر.

{{% /alert %}} 

Aspose.3D for .NET يسمح بتصدير مشهد 3D مثل potcloud باستخدام خاصية [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) من فئة [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). يوضح مقتطف الكود التالي كيفية استخدام هذه الوظيفة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var scene = new Scene(new Sphere());
scene.Save("Export3DSceneAsPointCloud.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
