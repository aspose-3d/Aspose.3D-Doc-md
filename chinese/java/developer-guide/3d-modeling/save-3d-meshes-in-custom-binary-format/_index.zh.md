---
title: 以自定义二进制格式保存 3D 网格
type: docs
weight: 30
url: /zh/java/save-3d-meshes-in-custom-binary-format/
description: Aspose.3D for Java API 支持打开任何受支持的 3D 文档，然后在二进制文件中写入网格。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 支持打开任何受支持的 3D 文档，然后在二进制文件中写入网格。

{{% /alert %}} 
##  **加载 3D 文件并以自定义二进制格式编写网格编程示例**
由 `Scene` 类中的RootNode成员公开的Accept方法允许访问每个子节点。下面的代码片段只允许转换网格。

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// load a 3D file
Scene scene = new Scene(MyDir + "test.fbx");
/*
* 3D format demonstration is simple
*
* struct File {
*   MeshBlock blocks[];
* };
*
* struct Vertex {
*   float x;
*   float y;
*   float z;
* };
*
* struct Triangle {
*   int a;
*   int b;
*   int c;
* };
*
* struct MeshBlock {
*   int numControlPoints;
*   int numTriangles;
*   Vertex vertices[numControlPoints];
*   Triangle faces[numTriangles];
* };
*/
// open file for writing in binary mode
try (DataOutputStream writer = new DataOutputStream(new BufferedOutputStream(new FileOutputStream(MyDir + "Save3DMeshesInCustomBinaryFormat_out"))))
{
    // visit each descent nodes
    scene.getRootNode().accept(new NodeVisitor(){
        @Override
        public boolean call(Node node) {
            try {
                for (Entity entity : node.getEntities()) {
                // only convert meshes, lights/camera and other stuff will be ignored
                if (!(entity instanceof IMeshConvertible))
                    continue;
                Mesh m = ((IMeshConvertible) entity).toMesh();
                List<Vector4> controlPoints = m.getControlPoints();
                // triangulate the mesh, so triFaces will only store triangle indices
                int[][] triFaces = PolygonModifier.triangulate(controlPoints, m.getPolygons());
                // gets the global transform matrix
                Matrix4 transform = node.getGlobalTransform().getTransformMatrix();
                // write number of control points and triangle indices
                writer.writeInt(controlPoints.size());
                writer.writeInt(triFaces.length);
                // write control points
                for (int i = 0; i < controlPoints.size(); i++) {
                    // calculate the control points in world space and save them to file
                    Vector4 cp = Matrix4.mul(transform, controlPoints.get(i));
                    writer.writeFloat((float) cp.x);
                    writer.writeFloat((float) cp.y);
                    writer.writeFloat((float) cp.z);
                }
                // write triangle indices
                for (int i = 0; i < triFaces.length; i++) {
                    writer.writeInt(triFaces[i][0]);
                    writer.writeInt(triFaces[i][1]);
                    writer.writeInt(triFaces[i][2]);
                }
            }
        } catch(Exception e) {
            e.printStackTrace();
        }
        return true;
    }
});
}
{{< /highlight >}}
