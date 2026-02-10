---
title: "إنشاء بيانات مظلية وثنائية الشكل لجميع الشبكات في نموذج 3D"
type: docs
weight: 10
url: /ar/java/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: "باستخدام Aspose.3D for Java API ، يمكن للمطورين إنشاء بيانات ماسية وثنائية الشكل لجميع الشبكات في أي مستند 3D مدعوم."
---
{{% alert color="primary" %}} 

باستخدام Aspose.3D for Java API ، يمكن للمطورين إنشاء بيانات ماسية وثنائية الشكل لجميع الشبكات في أي مستند 3D مدعوم.

{{% /alert %}} 
##  **Build angangent و Bالبيانات غير الطبيعية ل Msh**
لقد أضفنا طريقتين `buildTangentBinormal` في فئة `PolygonModifier`. إحدى الطرق تأخذ كائن فئة `Scene` كمعلمة والأخرى تأخذ كائن فئة `Mesh` كمعلمة كما هو موضح في مثال الرمز هذا:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene( MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.buildTangentBinormal(scene);
// Save 3D scene
scene.save(MyDir + "BuildTangentAndBinormalData_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
