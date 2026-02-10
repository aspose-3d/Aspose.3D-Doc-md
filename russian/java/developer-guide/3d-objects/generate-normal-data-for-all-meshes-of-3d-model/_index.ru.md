---
title: Генерировать нормальные данные для всех ячеек модели 3D
type: docs
weight: 40
url: /ru/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API поддерживает генерацию нормальных данных для всех ячеек модели 3D (без нормальных данных).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API поддерживает генерацию нормальных данных для всех ячеек модели 3D (без нормальных данных).

{{% /alert %}} 
##  **Генерировать нормальные данные для всех ячеек модели 3DS**
Метод generateNormal, представленный классом `PolygonModifier`, можно использовать для генерации нормальных данных для всех ячеек в файле 3DS. Если элемент VertexElementSmoothingGroup был определен в сетке, сгенерированные нормальные данные будут сглажены VertexElementSmoothingGroup.
###  **Образец программирования**
Этот пример кода загружает файл 3DS, посещает все узлы и создает нормальные данные для всех ячеек.

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
