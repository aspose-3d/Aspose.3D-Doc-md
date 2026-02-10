---
title: 3D modelinin tüm meshleri için normal veriler oluşturun
type: docs
weight: 40
url: /tr/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API has support of generating normal data for all meshes of 3D model (without the normal data).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API has support of generating normal data for all meshes of 3D model (without the normal data).

{{% /alert %}} 
##  **3DS modelinin tüm meshleri için normal veriler oluşturun**
`PolygonModifier` sınıfına maruz kalan genel boyut yöntemi, 3DS dosyasındaki tüm ağlar için normal veri oluşturmak için kullanılabilir. Vertexelementsmoothinggroup elemanı örgüde tanımlanmışsa, üretilen normal veriler vertexelement. inggroup tarafından düzeltilecektir.
###  **Programming ample ample**
Bu kod örneği 3DS dosyasını yükler, tüm düğümleri ziyaret eder ve tüm ağlar için normal veri oluşturur.

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
