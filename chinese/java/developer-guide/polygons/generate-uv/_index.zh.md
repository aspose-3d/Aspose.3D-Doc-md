---
title: 产生紫外线
type: docs
weight: 20
url: /zh/java/generate-uv/
description: Aspose.3D for Java 提供了用于公开GenerateUV方法的PolygonModifier类，您可以使用该类手动生成UV并将其与网格关联。
---
#  **产生紫外线**
Aspose.3D for Java 提供 `PolygonModifier` 类，该类公开GenerateUV方法，您可以使用该方法手动生成UV并将其与网格关联。以下代码段显示了生成和关联它的完整功能:

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
