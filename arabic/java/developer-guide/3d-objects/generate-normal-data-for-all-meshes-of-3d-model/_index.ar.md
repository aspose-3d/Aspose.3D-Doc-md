---
title: إنشاء بيانات عادية لجميع شبكات طراز 3D
type: docs
weight: 40
url: /ar/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API يدعم إنشاء بيانات عادية لجميع شبكات طراز 3D (بدون البيانات العادية).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API يدعم إنشاء بيانات عادية لجميع شبكات طراز 3D (بدون البيانات العادية).

{{% /alert %}} 
##  **إنشاء بيانات عادية لجميع شبكات طراز 3DS**
يمكن استخدام الطريقة generateNormal التي تعرضها فئة `PolygonModifier` لإنشاء بيانات عادية لجميع الشبكات في ملف 3DS. إذا تم تعريف عنصر المجموعة vertexelementsmث في الشبكة ، فسيتم تمهيد البيانات العادية التي تم إنشاؤها بواسطة مجموعة السلاسة vertextexementsementgrow.
###  **Pروغرامينغ ple وافرة**
يقوم مثال الرمز هذا بتحميل ملف 3DS ، وزيارة جميع العقد وإنشاء بيانات عادية لجميع الشبكات.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load a 3ds file, 3ds file doesn't have normal data, but it has smoothing group
Scene s = new Scene(MyDir + "camera.3ds");
// Visit all nodes and create normal data for all meshes
s.getRootNode().accept(new NodeVisitor() {
    @Override
    public boolean call(Node node) {
        Mesh mesh = (Mesh)node.getEntity();
        if (mesh != null)
        {
            VertexElementNormal normals = PolygonModifier.generateNormal(mesh);
            mesh.addElement(normals);
        }
        return true;
    }
});
{{< /highlight >}}
