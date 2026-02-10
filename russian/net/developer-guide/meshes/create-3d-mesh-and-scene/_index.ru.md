---
title: Создать сетку и сцену 3D
type: docs
weight: 10
url: /ru/net/create-3d-mesh-and-scene/
description: Сетка определяется набором контрольных точек и множеством n-сторонних многоугольников по мере необходимости. В этой статье объясняется, как определить сетку.
---
##  **Создайте сетку-куб 3D**
[`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) определяется набором контрольных точек и множеством n-односторонних многоугольников по мере необходимости. В этой статье объясняется, как определить `Mesh`.

Для того чтобы создать поверхность `Mesh`, нам нужно определить контрольные точки и многоугольники следующим образом:

- [Определите контрольные точки](/3d/ru/net/create-3d-mesh-and-scene/)
- [Создайте многоугольники с классом PolygonBuilder](/3d/ru/net/create-3d-mesh-and-scene/)
- [Создание полигонов](/3d/ru/net/create-3d-mesh-and-scene/)

Вот пример для прикрепления материала Фонга к узлу куба:
###  **Определите контрольные точки**
Сетка состоит из набора контрольных точек в пространстве и полигонов для описания поверхности сетки, чтобы создать сетку, нам нужно определить контрольные точки:

{{% alert color="primary" %}}

В контрольных точках всех геометрий в Aspose.3D используется однородная координата, поэтому в примере это `Vector4` вместо Vector3.

{{% /alert %}}

**Пример:**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize control points
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};

{{< /highlight >}}


###  **Создание полигонов**
Контрольные точки не отображаются, чтобы сделать куб видимым, нам нужно определить полигоны в каждой стороне:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Vector4[] controlPoints = DefineControlPoints();
            
// Initialize mesh object
Mesh mesh = new Mesh();
// Add control points to the mesh
mesh.ControlPoints.AddRange(controlPoints);
// Create polygons to mesh
// Front face (Z+)
mesh.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
mesh.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
mesh.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
mesh.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
mesh.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
mesh.CreatePolygon(new int[] { 3, 2, 6, 7 });

{{< /highlight >}}


###  **Создайте многоугольники с классом PolygonBuilder**
Мы также можем определить многоугольник по вершинам с классом `PolygonBuilder`:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Vector4[] controlPoints = DefineControlPoints();
            
// Initialize mesh object
Mesh mesh = new Mesh();

// Add control points to the mesh
mesh.ControlPoints.AddRange(controlPoints);
            
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
    builder.Begin();
    for (int v = 0; v < 4; v++)
        // The indice of vertice per each polygon
        builder.AddVertex(indices[vertexId++]);
    // Finished one polygon
    builder.End();
}


{{< /highlight >}}

Теперь он закончен, чтобы сделать сетку видимой, нам нужно подготовить узел для нее.
##  **Как триангулировать сетку**
Треугольная сетка полезна для игровой индустрии, потому что треугольная-единственный поддерживаемый примитив, который поддерживает оборудование GPU (нетреугольные данные триангулированы на уровне драйвера, что неэффективно при рендеринге в реальном времени)

{{% alert color="primary" %}}

В этой версии мы только триангулировали полигоны, так как это требуется для экспорта файлов 3ds, нормали/uvs и другие элементы вершины теряются во время этой процедуры, мы можем реализовать это в будущем.

{{% /alert %}}

В этом примере мы триангулируем Mesh, импортируя файл FBX и сохраняем его в формате FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.
           
// Initialize scene object
Scene scene = Scene.FromFile("document.fbx");
            
scene.RootNode.Accept(delegate(Node node)
{
    Mesh mesh = node.GetEntity<Mesh>();
    if (mesh != null)
    {
        // Triangulate the mesh
        Mesh newMesh = PolygonModifier.Triangulate(mesh);
        // Replace the old mesh
        node.Entity = mesh;
    }
    return true;
});
scene.Save("document.fbx");

{{< /highlight >}}
##  **Создайте сцену куба 3D**
В этом разделе показано, как добавить геометрию Mesh в сцену 3D. Пример кода помещает сцену куба и сохранения 3D в поддерживаемые форматы файлов.
###  **Создать узел куба**
Узел невидим, но можно визуализировать геометрию, прикрепленную к узлу.

{{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса Mesh, как там рассказано](https://docs.aspose.com/3d/net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Пример**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
            
// Initialize Node class object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();           

// Point node to the Mesh geometry
cubeNode.Entity = mesh;
            
// Add Node to a scene
scene.RootNode.ChildNodes.Add(cubeNode);           

// Save 3D scene in the supported file formats
scene.Save("CubeScene.fbx");           

{{< /highlight >}}

{{% alert color="primary" %}}

ПРИМЕЧАНИЕ: Сущности, прикрепленные к корневому узлу, обычно игнорируются в программном обеспечение CAD/CAM, поэтому нам нужно создать новый узел для рендеринга геометрии.

{{% /alert %}}
