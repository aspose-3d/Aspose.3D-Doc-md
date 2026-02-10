---
title: Generar datos normales para todas las mallas del modelo 3D
type: docs
weight: 40
url: /es/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API tiene soporte para generar datos normales para todas las mallas del modelo 3D (sin los datos normales).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte para generar datos normales para todas las mallas del modelo 3D (sin los datos normales).

{{% /alert %}} 
##  **Generar datos normales para todas las mallas del modelo 3DS**
El método generateNormal expuesto por la clase `PolygonModifier` se puede usar para generar datos normales para todas las mallas en un archivo 3DS. Si el elemento VertexElementSmoothingGroup se definió en la malla, los datos normales generados serán suavizados por VertexElementSmoothingGroup.
###  **Muestra de programación**
Este ejemplo de código carga un archivo 3DS, visita todos los nodos y crea datos normales para todas las mallas.

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
