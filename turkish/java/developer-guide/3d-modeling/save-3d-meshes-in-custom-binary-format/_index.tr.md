---
title: Save 3D Meshes in Custom Binary Format
type: docs
weight: 30
url: /tr/java/save-3d-meshes-in-custom-binary-format/
description: Aspose.3D for Java API desteklenen herhangi bir 3D belgesini açmak için desteğe sahiptir ve ardından ikili dosyadaki döküntüleri yazar.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API desteklenen herhangi bir 3D belgesini açmak için desteğe sahiptir ve ardından ikili dosyadaki döküntüleri yazar.

{{% /alert %}} 
##  **3D dosyasını yükleyin ve özel ikili format programlama örneğinde kafesler yazın**
`Scene` sınıfındaki root. üyesi tarafından maruz kalan yöntemi kabul etmek, her alt düğümünü ziyaret etmenizi sağlar. Aşağıdaki kod parçacığı sadece kafesleri dönüştürmeye izin verir.

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
