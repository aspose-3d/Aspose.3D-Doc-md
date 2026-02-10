---
title: Generar UV
type: docs
weight: 20
url: /es/java/generate-uv/
description: Aspose.3D for Java ofrece la clase PolygonModifier que expone el método GenerateUV, con el que puede generar UV manualmente y asociarlo con la malla.
---
#  **Generar UV**
Aspose.3D for Java ofrece la clase `PolygonModifier` que expone el método GenerateUV, con el que puede generar UV manualmente y asociarlo con la malla. El siguiente fragmento de código muestra la funcionalidad completa para generarlo y asociarlo:

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
