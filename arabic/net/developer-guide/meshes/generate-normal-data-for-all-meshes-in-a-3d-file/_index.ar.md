---
title: إنشاء بيانات عادية لجميع الشبكات في ملف 3D
type: docs
weight: 17
url: /ar/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: باستخدام Aspose.3D for .NET ، يمكن للمطورين إنشاء بيانات عادية لجميع الشبكات في أي طراز 3D (بدون البيانات العادية).
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يمكن للمطورين إنشاء بيانات عادية لجميع الشبكات في أي طراز 3D (بدون البيانات العادية).

{{% /alert %}}
##  **إنشاء بيانات عادية لجميع الشبكات في ملف 3DS**
يمكن استخدام طريقة `GenerateNormal` التي تعرضها فئة [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) لإنشاء بيانات عادية لجميع الشبكات في ملف 3DS. إذا تم تحديد عنصر `VertexElementSmoothingGroup` في الشبكة ، فسيتم تنعيم البيانات العادية التي تم إنشاؤها بواسطة `VertexElementSmoothingGroup`.
###  **Pروغرامينغ ple وافرة**
يقوم مثال الرمز هذا بتحميل ملف 3DS ، وزيارة جميع العقد وإنشاء بيانات عادية لجميع الشبكات.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3ds file, 3ds file doesn't have normal data, but it has smoothing group
            Scene s = new Scene(RunExamples.GetDataFilePath("camera.3ds"));
            // Visit all nodes and create normal data for all meshes
            s.RootNode.Accept(delegate(Node n)
            {
                Mesh mesh = n.GetEntity<Mesh>();
                if (mesh != null)
                {
                    VertexElementNormal normals = PolygonModifier.GenerateNormal(mesh);
                    mesh.VertexElements.Add(normals);
                }
                return true;
            });

{{< /highlight >}}
