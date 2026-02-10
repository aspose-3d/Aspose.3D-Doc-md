---
title: إنشاء بيانات مظلية وثنائية الشكل لجميع الشبكات في نموذج 3D
type: docs
weight: 30
url: /ar/net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: باستخدام Aspose.3D for .NET API ، يمكن للمطورين إنشاء بيانات ظلية وثنائية لجميع الشبكات في أي ملف 3D مدعوم.
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](http://products.aspose.com/3d/net) API ، يمكن للمطورين إنشاء بيانات ظلية وثنائية لجميع الشبكات في أي ملف 3D مدعوم.

{{% /alert %}}
##  **Build angangent و Bالبيانات غير الطبيعية ل Msh**
لقد أضفنا طريقتين buildtanentbinormal في فئة [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier). إحدى الطرق تأخذ كائن فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) كمعلمة والأخرى تأخذ كائن فئة [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) كمعلمة كما هو موضح في مثال الرمز هذا:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Load an existing 3D file
Scene scene = new Scene(RunExamples.GetDataFilePath("document.fbx"));
// Triangulate a scene
PolygonModifier.BuildTangentBinormal(scene);
// Save 3D scene
scene.Save(RunExamples.GetOutputFilePath("BuildTangentAndBinormalData_out.fbx"), FileFormat.FBX7400ASCII);

{{< /highlight >}}
