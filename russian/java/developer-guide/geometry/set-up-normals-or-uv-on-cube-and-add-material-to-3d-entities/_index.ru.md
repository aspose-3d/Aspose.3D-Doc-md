---
title: Настройте нормали или UV на Cube и добавьте материал в сущности 3D
type: docs
weight: 60
url: /ru/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java предлагает управлять нормалями и УФ на геометрических фигурах. Сетка хранит ключевые свойства для каждой вершины, положения в пространстве и его нормали, известной как вектор, перпендикулярный исходной поверхности. Нормаль является основным для отсчетов затенения и должна быть единичным вектором. Большинство форматов сетки также поддерживают некоторую форму УФ-координат, которые являются отдельным 2D представлением сетки, «развернутой», чтобы показать, какую часть двумерной текстурной карты применять к различным многоугольникам сетки.
---
{{% alert color="primary" %}}

Aspose.3D for Java предлагает управлять нормалями и УФ на геометрических фигурах. Сетка хранит ключевые свойства для каждой вершины, положения в пространстве и его нормали, известной как вектор, перпендикулярный исходной поверхности. Нормаль является основным для отсчетов затенения и должна быть единичным вектором. Большинство форматов сетки также поддерживают некоторую форму УФ-координат, которые являются отдельным 2D представлением сетки, «развернутой», чтобы показать, какую часть двумерной текстурной карты применять к различным многоугольникам сетки.

{{% /alert %}} {{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса Mesh, как рассказано здесь](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/), а затем указать узел на геометрию Mesh, создав сцену 3D.

{{% /alert %}}
##  **Создание нормальных векторов**
Для того, чтобы иметь хороший визуальный вид на освещение, нам нужно указать нормальную информацию для каждой вершины. Чтобы получить лучшую детализацию, мы также можем использовать нормальную и диффузную карту (используйте карту тени/зеркала) для выполнения нормального/цветного пикселя. Информация для каждой вершины, такая как нормальный цвет или цвет вершины, достигается VertexElement. В Aspose.3D мы можем сопоставить дополнительную информацию в контрольные точки/вершину полигона/полигон/ребро, выборку для определения нормалей для вершины:

{{< highlight "java" >}}
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}


8 нормальных векторов сопоставляются с 8 контрольными точками напрямую, в следующем примере мы продемонстрируем немного более сложный сценарий.
##  **Создание УФ-координат**
Здесь мы определили только 4 УФ-координаты, но применили их к 24 вершинам многоугольника (6 грани * 4 вершины на многоугольник) с помощью индексов.
Aspose.3D предоставляет 5 режимов сопоставления:

- **ControlPoint**-Каждый данные сопоставляется с контрольной точкой геометрии.
- **Полигонвертекс**-Данные отображаются на вершину многоугольника.
- **Полигон**-Данные отображаются на полигон.
- **Край**-Данные сопоставляется с краем.
- **AllSame**-Один данные, отображаемые на всю геометрию.



{{< highlight "java" >}}
// UVs
Vector4[] uvs = new Vector4[]
{
    new Vector4( 0.0, 1.0,0.0, 1.0),
    new Vector4( 1.0, 0.0,0.0, 1.0),
    new Vector4( 0.0, 0.0,0.0, 1.0),
    new Vector4( 1.0, 1.0,0.0, 1.0)
};
// Indices of the uvs per each polygon
int[] uvsId = new int[]
{
    0,1,3,2,2,3,5,4,4,5,7,6,6,7,9,8,1,10,11,3,12,0,2,13
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Create UVset
VertexElementUV elementUV = mesh.createElementUV(TextureMapping.DIFFUSE, MappingMode.POLYGON_VERTEX, ReferenceMode.INDEX_TO_DIRECT);
// Copy the data to the UV vertex element
elementUV.setData(uvs);
elementUV.setIndices(uvsId);
{{< /highlight >}}
##  **Добавить материалы в объекты 3D**
Aspose.3D for Java позволяет разработчикам использовать алгоритм затенения для точного затенения и выделения. Фонг имеет несколько входов карты, которые мы можем использовать для маскировки эффекта для узла. Физически ориентированный рендеринг (PBR) учитывает некоторые физические свойства объектов, такой подход обеспечивает внешний вид материалов, как в реальном мире.
###  **Материал Phong с текстурой для куба**
Когда УФ-координаты готовы к использованию, мы можем нанести текстуру на поверхность сетки, используя материал. Только цвет вершины не может описать детали поверхности, это то, для чего использовались материалы. Вот пример для прикрепления материала Фонга к узлу куба:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize cube node object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cubeNode.setEntity(mesh);
// Add cube to the scene
scene.getRootNode().addChildNode(cubeNode);
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
// Initiallize Texture object
Texture diffuse = new Texture();
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Set local file path
diffuse.setFileName(MyDir + "surface.dds");
// Set Texture of the material
mat.setTexture(Material.MAP_DIFFUSE, diffuse);
// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.setFileName("embedded-texture.png");
// Set binary content
diffuse.setContent(Files.readAllBytes(Paths.get(MyDir, "aspose-logo.jpg")));
// Set color
mat.setSpecularColor(new Vector3(1, 0, 0));
// Set brightness
mat.setShininess(100);
// Set material property of the cube object
cubeNode.setMaterial(mat);
MyDir = MyDir + RunExamples.getOutputFilePath("MaterialToCube.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


Мы указали отображение диффузной текстуры и зеркальный цвет с параметром сияния.
###  **Применить материал для физического отендинга (PBR) к коробке**
PBR играет ключевую роль в визуальных эффектах игрового движка с его эффективной и реалистичной визуализацией взаимодействий между светом и поверхностью посредством ослабления яркости и рассеяния отраженного света. Разработчики могут использовать Aspose.3D API, чтобы применить материал PBR к 3D объектам в сцене. Этот пример кода демонстрирует, как создать объект Box, а затем применить материал PBR.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}
