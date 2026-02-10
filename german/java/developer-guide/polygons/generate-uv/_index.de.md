---
title: Erzeugen Sie UV
type: docs
weight: 20
url: /de/java/generate-uv/
description: Aspose.3D for Java bietet PolygonModifier-Klasse, die GenerateUV-Methode enthüllt, mit der Sie UV manuell erzeugen und mit dem Netz verknüpfen können.
---
#  **Erzeugen Sie UV**
Aspose.3D for Java bietet `PolygonModifier` Klasse, die GenerateUV-Methode enthüllt, mit der Sie UV manuell erzeugen und mit dem Netz verknüpfen können. Das folgende Code-Snippet zeigt die vollständige Funktional ität, um es zu generieren und zu verknüpfen:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
Scene scene = new Scene();
//since all primitive entities in Aspose.3D will have builtin UV generation
//here we manually remove it to assume we have a mesh without UV data
Mesh mesh = (new Box()).toMesh();
mesh.getVertexElements().remove(mesh.getElement(VertexElementType.UV));

//then we can manually generate UV for it
VertexElement uv = PolygonModifier.generateUV(mesh);
//generated UV data is not associated with the mesh, we should manually do this
mesh.addElement(uv);
//put it to the scene
Node node = scene.getRootNode().createChildNode(mesh);
//then save it
scene.save(MyDir + "test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}
