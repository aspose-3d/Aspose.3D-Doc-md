---
title: تحويل جميع المضلعات إلى مثلثات في نموذج 3D
type: docs
weight: 10
url: /ar/java/convert-all-polygons-to-triangles-in-3d-model/
description: Aspose.3D for Java API يدعم تحويل جميع المضلعات إلى مثلثات في أي مستند 3D مدعوم.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API يدعم تحويل جميع المضلعات إلى مثلثات في أي مستند 3D مدعوم.

{{% /alert %}} 
##  **Convert جميع أوليغونس Pإلى riri**
لقد أضفنا حمولة زائدة أخرى من طريقة التثليث في فئة `PolygonModifier` والتي تأخذ كائن فئة `Scene` كمعلمة كما هو موضح في مثال الرمز هذا:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load an existing 3D file
Scene scene = new Scene(MyDir + "document.fbx");
// Triangulate a scene
PolygonModifier.triangulate(scene);
// Save 3D scene
scene.save(MyDir + "triangulated_out.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
