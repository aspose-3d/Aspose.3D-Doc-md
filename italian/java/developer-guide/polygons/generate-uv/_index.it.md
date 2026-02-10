---
title: Generare UV
type: docs
weight: 20
url: /it/java/generate-uv/
description: Aspose.3D for Java offre la classe PolygonModifier che espone il metodo GenerateUV, con il quale è possibile generare manualmente UV e associarlo alla mesh.
---
#  **Generare UV**
Aspose.3D for Java offre una classe `PolygonModifier` che espone il metodo GenerateUV, con il quale è possibile generare manualmente UV e associarlo alla mesh. Il seguente frammento di codice mostra la funzionalità completa per generarlo e associarlo:

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
