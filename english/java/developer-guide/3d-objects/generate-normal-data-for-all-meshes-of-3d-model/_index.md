---
title: Generate Normal Data for All Meshes of 3D Model
type: docs
weight: 40
url: /java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API has support of generating normal data for all meshes of 3D model (without the normal data).
---

{{% alert color="primary" %}} 

Aspose.3D for Java API has support of generating normal data for all meshes of 3D model (without the normal data).

{{% /alert %}} 
## **Generate Normal Data for All Meshes of 3DS Model**
The generateNormal method exposed by the `PolygonModifier` class can be used to generate normal data for all meshes in a 3DS file. If VertexElementSmoothingGroup element was defined in the mesh, the generated normal data will get smoothed by the VertexElementSmoothingGroup.
### **Programming Sample**
This code example loads a 3DS file, visit all nodes and create normal data for all meshes.

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
