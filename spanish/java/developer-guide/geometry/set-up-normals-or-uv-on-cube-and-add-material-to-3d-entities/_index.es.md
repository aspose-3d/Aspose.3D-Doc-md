---
title: Configurar normales o UV en cubo y agregar material a entidades 3D
type: docs
weight: 60
url: /es/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java ofrece administrar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice, posición en el espacio y su normal, conocida como vector perpendicular a la superficie original. La normal es importante para los recuentos de sombreado y debe ser un vector unitario. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2D separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.
---
{{% alert color="primary" %}}

Aspose.3D for Java ofrece administrar normales y UV en las formas geométricas. Una malla almacena las propiedades clave para cada vértice, posición en el espacio y su normal, conocida como vector perpendicular a la superficie original. La normal es importante para los recuentos de sombreado y debe ser un vector unitario. La mayoría de los formatos de malla también admiten alguna forma de coordenadas UV que son una representación 2D separada de la malla "desplegada" para mostrar qué parte de un mapa de textura bidimensional aplicar a diferentes polígonos de la malla.

{{% /alert %}} {{% alert color="primary" %}}

El objeto de clase `Mesh` se está utilizando en el código. Podemos [Crear un objeto de clase Mesh como se narra aquí](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) y luego apuntar el nodo a la geometría de malla creando una escena 3D.

{{% /alert %}}
##  **Crear vectores normales**
Para tener un buen aspecto visual de la iluminación, necesitamos especificar información normal para cada vértice. Para tener los mejores detalles, también podemos usar el mapa normal y difuso (use sombra/mapa especular) para realizar por píxel normal/color. VertexElement logra una información por vértice como el color normal o de vértice. En Aspose.3D podemos asignar información adicional a puntos de control/vértice de polígono/arista, una muestra para definir normales para el vértice:

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


Los 8 vectores normales se asignan a 8 puntos de control directamente, en el siguiente ejemplo, demostraremos un escenario un poco más complejo.
##  **Crear coordenadas UV**
Aquí, solo definimos 4 coordenadas UV, pero las aplicamos a 24 vértices poligonales (6 caras * 4 vértices por polígono) mediante el uso de índices.
Aspose.3D proporciona 5 modos de asignación:

- **Punto de control**: Cada dato se asigna al punto de control de la geometría.
- **Poligonvértice**-Los datos se asignan al vértice del polígono.
- **Polígono**-Los datos se asignan al polígono.
- **Borde**-Los datos se asignan al borde.
- **AllSame**-Un dato mapeado a toda la geometría.



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
##  **Agregar materiales a objetos 3D**
Aspose.3D for Java permite a los desarrolladores utilizar el algoritmo de sombreado para un sombreado y resaltado precisos. El Phong tiene varias entradas de mapa que podemos usar para enmascarar el efecto al nodo. Physically Based Rendering (PBR) tiene en cuenta algunas propiedades físicas de los objetos, tal enfoque proporciona la apariencia de los materiales como en el mundo real.
###  **Material Phong con textura para cubo**
Cuando las coordenadas UV están listas para usar, podemos aplicar una textura en la superficie de la malla utilizando material. Solo el color de los vértices no puede describir los detalles de la superficie, para eso se utilizaron los materiales. Aquí hay un ejemplo para adjuntar un material Phong al nodo del cubo:

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


Especificamos el mapeo de textura difusa y un color especular con un parámetro de brillo.
###  **Aplicar material de rendering basado en la física (PBR) a una caja**
PBR juega un papel clave para las imágenes del motor del juego, con su representación eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar Aspose.3D API para aplicar material de PBR a objetos 3D en una escena. En este ejemplo de código se muestra cómo crear un objeto Box y, a continuación, aplicar el material PBR.

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
