---
title: Настройте нормали или УФ на Кубе и добавьте материал в сущности 3D
type: docs
weight: 20
url: /ru/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Как создать нормали или uv данные на сетке в Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET предлагает управлять нормалями и УФ на геометрических фигурах. Сетка хранит ключевые свойства для каждой вершины-ее положение в пространстве и нормаль, вектор, перпендикулярный исходной поверхности. Нормальный является основным для количества затенений. Нормали должны быть единичными векторами. Большинство форматов сетки также поддерживают некоторую форму УФ-координат, которые представляют собой отдельное 2d представление сетки, «развернутой», чтобы показать, какую часть двумерной текстурной карты применять к различным полигонам сетки.

{{% /alert %}} {{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса Mesh, как там рассказано](/3d/ru/net/create-3d-mesh-and-scene/), а затем указать узел на геометрию Mesh с помощью [Создание сцены 3D](/3d/ru/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Создание нормальных векторов**
Чтобы иметь хороший визуальный вид на освещение, нам нужно указать нормальную информацию для каждой вершины, чтобы иметь лучшие детали, мы также можем использовать нормальную и диффузную карту (конечно, вы можете использовать теневую/зеркальную карту) для выполнения на пиксель нормаль/цвет. Информация для каждой вершины, такая как нормальный цвет или цвет вершины, достигается VertexElement. В Aspose.3D мы можем сопоставить дополнительную информацию в контрольные точки/вершину полигона/полигон/ребро, выборку для определения нормалей для вершины:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
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
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;
// Copy the data to the vertex element
elementNormal.Data.AddRange(normals);

{{< /highlight >}}

8 нормальных векторов сопоставляются с 8 контрольными точками напрямую, в следующем примере мы продемонстрируем немного более сложный сценарий.
##  **Создание УФ-координат**
Здесь мы определили только 4 УФ-координаты, но применили их к 24 вершинам многоугольника (6 грани * 4 вершины на многоугольник) с помощью индексов.
Aspose.3D предоставляет 5 режимов сопоставления:

- `ControlPoint` -все данные сопоставляются с контрольной точкой геометрии.
- `PolygonVertex` -данные отображаются в вершину многоугольника.
- `Polygon` -данные сопоставлены с многоугольником.
- `Edge` -данные сопоставлены с ребром.
- `AllSame` -один из данных сопоставлен со всей геометрией.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
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
Mesh mesh = Common.CreateMeshUsingPolygonBuilder();

// Create UVset
VertexElementUV elementUV = mesh.CreateElementUV(TextureMapping.Diffuse, MappingMode.PolygonVertex, ReferenceMode.IndexToDirect);
// Copy the data to the UV vertex element 
elementUV.Data.AddRange(uvs);
elementUV.Indices.AddRange(uvsId);

{{< /highlight >}}
##  **Добавить материалы в объекты 3D**
Aspose.3D for .NET позволяет разработчикам использовать алгоритм затенения для точного затенения и выделения. Фонг имеет несколько входов карты, которые мы можем использовать для маскировки эффекта для узла. Физически ориентированный рендеринг (PBR) учитывает некоторые физические свойства объектов, такой подход обеспечивает внешний вид материалов, как в реальном мире.
###  **Материал Phong с текстурой для куба**
Когда УФ-координаты готовы к использованию, мы можем нанести текстуру на поверхность сетки, используя материал. Только цвет вершины не может описать детали поверхности, это то, для чего использовались материалы. Вот пример для прикрепления материала Фонга к узлу куба:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize scene object
Scene scene = new Scene();
            
// Initialize cube node object
Node cubeNode = new Node("cube");

// Call Common class create mesh using polygon builder method to set mesh instance 
Mesh mesh = Common.CreateMeshUsingPolygonBuilder(); 
         
// Point node to the mesh
cubeNode.Entity = mesh;
            
// Add cube to the scene
scene.RootNode.ChildNodes.Add(cubeNode);
            
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
            
// Initiallize Texture object
Texture diffuse = new Texture();
            
// The path to the documents directory.
            
// Set local file path
diffuse.FileName = RunExamples.GetOutputFilePath("surface.dds");

// Set Texture of the material
mat.SetTexture("DiffuseColor", diffuse);

// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.FileName = "embedded-texture.png";
// Set binary content
diffuse.Content = File.ReadAllBytes(RunExamples.GetDataFilePath("aspose-logo.jpg"));

// Set color
mat.SpecularColor = new Vector3(Color.Red);

// Set brightness
mat.Shininess = 100;

// Set material property of the cube object
cubeNode.Material = mat;
            
// Save 3D scene in the supported file formats
scene.Save("MaterialToCube.fbx");

{{< /highlight >}}

Мы указали отображение диффузной текстуры и зеркальный цвет с параметром сияния.
###  **Применить материал для физического отендинга (PBR) к коробке**
PBR играет ключевую роль в визуальных эффектах игрового движка с его эффективной и реалистичной визуализацией взаимодействий между светом и поверхностью посредством ослабления яркости и рассеяния отраженного света. Разработчики могут использовать Aspose.3D API, чтобы применить материал PBR к 3D объектам в сцене. Этот пример кода демонстрирует, как создать объект Box, а затем применить материал PBR.

**.NET, C#**

{{< highlight "java" >}}

 // initialize a scene

Scene scene = new Scene();

// initialize PBR material object

PbrMaterial mat = new PbrMaterial();

// an almost metal material

mat.MetallicFactor = 0.9;

// material surface is very rough

mat.RoughnessFactor = 0.9;

// create a box to which the material will be applied

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

// save 3d scene into STL format

scene.Save(@"C:\3D\PBR_Material_Box_Out.stl", FileFormat.STLASCII);

{{< /highlight >}}
