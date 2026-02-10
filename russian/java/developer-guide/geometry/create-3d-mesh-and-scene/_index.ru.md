---
title: Создать сетку и сцену 3D
type: docs
weight: 40
url: /ru/java/create-3d-mesh-and-scene/
description: Сетка определяется набором контрольных точек и множеством n-сторонних многоугольников по мере необходимости. В этой статье объясняется, как определить сетку.
---
##  **Создайте сетку-куб 3D**
`Mesh` определяется набором контрольных точек и множеством n-односторонних многоугольников по мере необходимости. В этой статье объясняется, как определить `Mesh`.

Для того чтобы создать поверхность `Mesh`, нам нужно определить контрольные точки и многоугольники следующим образом:

- [Определите контрольные точки](/3d/ru/java/create-3d-mesh-and-scene-html/)
- [Создайте многоугольники с классом PolygonBuilder](/3d/ru/java/create-3d-mesh-and-scene-html/)
- [Создание полигонов](/3d/ru/java/create-3d-mesh-and-scene-html/)

Вот пример для прикрепления материала Фонга к узлу куба:
###  **Определите контрольные точки**
Сетка состоит из набора контрольных точек в пространстве и полигонов для описания поверхности сетки, чтобы создать сетку, нам нужно определить контрольные точки:

{{% alert color="primary" %}} 

В контрольных точках всех геометрий в Aspose.3D используется однородная координата, поэтому в примере это `Vector4` вместо `Vector3`.

{{% /alert %}} 

**Пример:**

{{< highlight "java" >}}
// Initialize control points
Vector4List controlPoints = new Vector4List(8);
controlPoints.add(new Vector4( -5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, 5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, 5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 0.0, -5.0, 1.0));
controlPoints.add(new Vector4( 5.0, 10.0, -5.0, 1.0));
controlPoints.add(new Vector4( -5.0, 10.0, -5.0, 1.0));
{{< /highlight >}}



###  **Создание полигонов**
Контрольные точки не отображаются, чтобы сделать куб видимым, нам нужно определить полигоны в каждой стороне:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
// Create polygons to mesh
// Front face (Z+)
mesh.createPolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
mesh.createPolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
mesh.createPolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
mesh.createPolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
mesh.createPolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
mesh.createPolygon(new int[] { 3, 2, 6, 7 });
{{< /highlight >}}



###  **Создайте многоугольники с классом PolygonBuilder**
Мы также можем определить многоугольник по вершинам с классом PolygonBuilder:

{{< highlight "java" >}}
List<Vector4> controlPoints = defineControlPoints();
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.getControlPoints().addAll(controlPoints);
// Indices of the vertices per each polygon
int[] indices = new int[]
{
    0,1,2,3, // Front face (Z+)
    1,5,6,2, // Right side (X+)
    5,4,7,6, // Back face (Z-)
    4,0,3,7, // Left side (X-)
    0,4,5,1, // Bottom face (Y-)
    3,2,6,7 // Top face (Y+)
};
int vertexId = 0;
PolygonBuilder builder = new PolygonBuilder(mesh);
for (int face = 0; face < 6; face++)
{
    // Start defining a new polygon
    builder.begin();
    for (int v = 0; v < 4; v++)
        // The indice of vertice per each polygon
        builder.addVertex(indices[vertexId++]);
    // Finished one polygon
    builder.end();
}
{{< /highlight >}}

Теперь он закончен, чтобы сделать сетку видимой, нам нужно подготовить узел для нее.
##  **Как триангулировать сетку**
Треугольная сетка полезна для игровой индустрии, потому что треугольная-единственный поддерживаемый примитив, который поддерживает оборудование GPU (нетреугольные данные триангулированы на уровне драйвера, что неэффективно при рендеринге в реальном времени)

{{% alert color="primary" %}} 

В этой версии мы только триангулировали полигоны, так как это требуется для экспорта файлов 3ds, нормали/uvs и другие элементы вершины теряются во время этой процедуры, мы можем реализовать это в будущем.

{{% /alert %}} 

В этом примере мы триангулируем Mesh, импортируя файл FBX и сохраняем его в формате FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize scene object
Scene scene = new Scene();
scene.open(MyDir + "document.fbx");
scene.getRootNode().accept(new NodeVisitor() {
    @Override
    public boolean call(Node node) {
        Mesh mesh = (Mesh)node.getEntity();
        if (mesh != null)
        {
            // Triangulate the mesh
            Mesh newMesh = PolygonModifier.triangulate(mesh);
            // Replace the old mesh
            node.setEntity(newMesh);
        }
        return true;
    }
});
MyDir = MyDir + RunExamples.getOutputFilePath("document.fbx");
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Создайте сцену куба 3D**
В этом разделе показано, как добавить геометрию Mesh в сцену 3D. Пример кода помещает сцену куба и сохранения 3D в поддерживаемые форматы файлов.
###  **Создать узел куба**
Узел невидим, но можно визуализировать геометрию, прикрепленную к узлу.

{{% alert color="primary" %}} 

В коде используется объект класса Mesh. Мы можем [Создать объект класса Mesh, как там рассказано](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Пример:**

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the Mesh geometry
cubeNode.setEntity(mesh);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("CubeScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}

{{% alert color="primary" %}} 

ПРИМЕЧАНИЕ: Сущности, прикрепленные к корневому узлу, обычно игнорируются в программном обеспечение CAD/CAM, поэтому нам нужно создать новый узел для рендеринга геометрии.

{{% /alert %}}
