---
title: Преобразование сетки в треугольную сетку и примитивной формы в сетку
type: docs
weight: 20
url: /ru/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API поддерживает преобразование сетки в треугольную сетку с пользовательским расположением памяти вершины. Пользовательская компоновка памяти Vertex определяется динамически классом VertexDeclarion в примерах кода.
---
##  **Конвертировать Mesh в треугольную сетку с пользовательской компоновкой памяти Vertex**
Aspose.3D for Java API поддерживает преобразование сетки в треугольную сетку с пользовательским расположением памяти вершины. Пользовательская компоновка памяти Vertex определяется динамически классом `VertexDeclaration` в примерах кода.

{{% alert color="primary" %}}

Этот раздел справки создает сетки из коробки и сферы, чтобы код был исчерпывающим и коротким. Разработчики могут создавать сетку вручную, как рассказывают в этой теме справки: [Создайте сетку-куб 3D](/3d/ru/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Разработчики могут преобразовывать сетку в треугольную сетку, потому что любая сложная (поверхностная) структура может быть представлена в виде группы треугольников. Треугольник-самая атомарная геометрия. Таким образом, он используется как база практически для чего угодно. Этот пример кода преобразует Box в треугольную сетку с пользовательским макетом памяти.



{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("box");
// Get mesh of the Box
Mesh box = (new Box()).toMesh();
// Create a customized vertex layout
VertexDeclaration vd = new VertexDeclaration();
VertexField position = vd.addField(VertexFieldDataType.F_VECTOR4, VertexFieldSemantic.POSITION);
vd.addField(VertexFieldDataType.F_VECTOR3, VertexFieldSemantic.NORMAL);
// Get a triangle mesh
TriMesh triMesh = TriMesh.fromMesh(box);
// ExEnd:ConvertBoxMeshtoTriangleMeshCustomMemoryLayout
// Point node to the Mesh geometry
cubeNode.setEntity(box);
// Add Node to a scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir() + RunExamples.getOutputFilePath("BoxToTriangleMeshCustomMemoryLayoutScene.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}
##  **Преобразование примитивной формы в сетку**
Aspose.3D for Java API поддерживает преобразование любой примитивной фигуры в сетку. Примитивные формы включают в себя самые основные и используемые объекты, такие как коробка, сфера, плоскость, цилиндр и тор.

{{% alert color="primary" %}}

Любой класс, реализующий интерфейс IMESHConvertible, может быть преобразован в mesh при экспорте в любой формат файла 3D.

{{% /alert %}}
###  **Преобразование Sphere Primitive в Mesh**
Сфера-это идеально круглый геометрический объект в трехмерном пространстве, который появляется повсюду, от спортивных мячей до планет в космосе. Давайте использовать примитив Sphere для создания сетки.
Пример кода ниже преобразует Сферу в сетку.

{{< highlight "java" >}}
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
// Convert a Sphere to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Конвертировать Box в Mesh**
Коробка описывает различные контейнеры и емкости для постоянного использования в качестве хранилища или для временного использования, часто для транспортировки содержимого. Давайте использовать примитивный ящик для создания сетки. Пример кода ниже преобразует Box в сетку.

{{< highlight "java" >}}
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Преобразование плоскости в сетку**
Плоскость тянется бесконечно без толщины. Примером плоскости является плоскость координат. Давайте использовать примитив Plane для создания сетки. Пример кода ниже преобразует плоскость в сетку.

{{< highlight "java" >}}
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
// Convert a Plane to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Преобразование цилиндра в сетку**
Цилиндр-одна из самых основных криволинейных геометрических форм, поверхность, образованная точками на фиксированном расстоянии от заданной прямой линии, оси цилиндра. Его можно использовать во многих местах, например, в качестве стойки перед домом или в качестве приводного вала автомобиля. Для создания сетки позволяет использовать примитивный цилиндр. Пример кода ниже преобразует цилиндр в сетку.

{{< highlight "java" >}}
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
// Convert a Cylinder to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Конвертировать Torus в Mesh**
Тор-это поверхность вращения, порожденная вращением окружности в трехмерном пространстве вокруг оси, копланарной окружности. Если ось вращения не касается круга, поверхность имеет форму кольца и называется тор вращения. Давайте использовать примитив Torus для создания сетки. Пример кода ниже преобразует Torus в сетку.

{{< highlight "java" >}}
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
// Convert a Torus to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
