---
title: Configurar normales o UV en el cubo y agregar material a entidades 3D
type: docs
weight: 20
url: /es/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Cómo crear datos normales o uv en una malla en Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET ofrece administrar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice son su posición en el espacio y su normal, un vector perpendicular a la superficie original. Lo normal es importante para los recuentos de sombreado. Las normales deben ser vectores unitarios. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2d separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.

{{% /alert %}} {{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos [Crear un objeto de clase Mesh como se narra allí](/3d/es/net/create-3d-mesh-and-scene/) y luego apuntar el nodo a la geometría de malla por [Creación de una escena 3D](/3d/es/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Crear vectores normales**
Para tener un buen aspecto visual en la iluminación, necesitamos especificar información de normales para cada vértice, para tener mejores detalles, también podemos usar mapa normal y difuso (seguro que puede usar mapa de sombra/especular) para realizar por píxel normal/color. VertexElement logra una información por vértice como el color normal o de vértice. En Aspose.3D podemos asignar información adicional a puntos de control/vértice de polígono/arista, una muestra para definir normales para el vértice:

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

Los 8 vectores normales se asignan a 8 puntos de control directamente, en el siguiente ejemplo, demostraremos un escenario un poco más complejo.
##  **Crear coordenadas UV**
Aquí, solo definimos 4 coordenadas UV, pero las aplicamos a 24 vértices poligonales (6 caras * 4 vértices por polígono) mediante el uso de índices.
Aspose.3D proporciona 5 modos de asignación:

- `ControlPoint` -cada dato se asigna al punto de control de la geometría.
- `PolygonVertex` -los datos se asignan al vértice del polígono.
- `Polygon` -los datos se asignan al polígono.
- `Edge` -los datos se asignan al borde.
- `AllSame` -un dato asignado a toda la geometría.



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
##  **Agregar materiales a objetos 3D**
Aspose.3D for .NET permite a los desarrolladores utilizar el algoritmo de sombreado para un sombreado y resaltado precisos. El Phong tiene varias entradas de mapa que podemos usar para enmascarar el efecto al nodo. Physically Based Rendering (PBR) tiene en cuenta algunas propiedades físicas de los objetos, tal enfoque proporciona la apariencia de los materiales como en el mundo real.
###  **Material Phong con textura para cubo**
Cuando las coordenadas UV están listas para usar, podemos aplicar una textura en la superficie de la malla utilizando material. Solo el color de los vértices no puede describir los detalles de la superficie, para eso se utilizaron los materiales. Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:

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

Especificamos el mapeo de textura difusa y un color especular con un parámetro de brillo.
###  **Aplicar material de rendering basado en la física (PBR) a una caja**
PBR juega un papel clave para las imágenes del motor del juego, con su representación eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar Aspose.3D API para aplicar material de PBR a objetos 3D en una escena. En este ejemplo de código se muestra cómo crear un objeto Box y, a continuación, aplicar el material PBR.

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
