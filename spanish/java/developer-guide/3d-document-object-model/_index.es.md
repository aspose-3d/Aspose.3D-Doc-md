---
title: Aspose.3D Modelo de objetos de documento (DOM)
type: docs
weight: 20
url: /es/java/aspose-3d-document-object-model
description: Cada escena 3D puede comprender cualquier número de ventanas gráficas. Con Aspose.3D for Java API, los desarrolladores pueden capturar una o más ventanas gráficas en una sola captura de pantalla. Pueden renderizarlo en la aplicación Java basada en la GUI o en una imagen.
---
The Aspose.3D Document Object Model (DOM) is a powerful in-memory representation of a 3D scene. It provides developers with the ability to read, manipulate, and modify the content and formatting of a 3D scene programmatically.

En esta sección, exploraremos las clases clave del DOM Aspose.3D y sus relaciones. Al utilizar estas clases, puede obtener acceso programático a varios elementos dentro de una escena 3D.

Vamos a adentrarse en las principales clases del DOM Aspose.3D:

* **Escena**La clase Scene representa la raíz de la jerarquía de escena 3D. Sirve como contenedor para todos los demás elementos y proporciona métodos para manipular la escena en general.
* **Nodo**Los nodos son los bloques de construcción de una escena 3D. Representan objetos o entidades individuales dentro de la escena, como mallas, luces, cámaras o grupos. Los nodos pueden ser transformados, animados y texturizados.
* **Entidades**Las clases Entidades abarcan una amplia gama de objetos y elementos que componen una escena 3D. Incluye entidades como mallas, luces, cámaras, perfiles y más. Estas entidades sirven como bloques de construcción, permitiéndole crear escenas complejas combinándolas y manipulándolas mediante programación. La categoría Entidades proporciona acceso y control sobre estos elementos fundamentales de una escena 3D.
* **Materiales**Las clases de materiales giran en torno a la definición de las propiedades visuales de los objetos dentro de una escena 3D. Proporciona herramientas para crear, modificar y controlar materiales mediante programación, que determinan cómo la luz interactúa con las superficies. Al ajustar propiedades como el color, la textura, la transparencia y el reflejo, puede lograr varios efectos visuales y personalizar la apariencia de sus modelos 3D.
* **Animaciones**Las clases de animación se centran en crear y controlar el movimiento y las transformaciones dentro de una escena 3D. Permite definir y manipular animaciones mediante programación, permitiendo que los objetos se muevan, roten, escalen o cambien sus propiedades con el tiempo. Con esta categoría, puedes traer elementos dinámicos e interactivos a tus escenas de 3D.

Al utilizar las clases DOM Aspose.3D mencionadas anteriormente, puede interactuar y manipular programáticamente el contenido y la estructura de una escena 3D. Esto proporciona flexibilidad y control cuando se trabaja con modelos 3D en sus aplicaciones.


## Estructura de la escena

Cuando Aspose.3D lee un archivo 3D en la memoria, genera objetos de varios tipos para representar los diferentes elementos dentro de la escena 3D.


La estructura de la escena en Aspose.3D sigue el patrón de diseño compuesto, que ofrece flexibilidad y organización:

 Los nodos sirven como contenedores que pueden contener otros nodos, lo que permite agrupar diferentes objetos dentro de la escena.
 * Cada nodo puede tener su propia transformación, que también se aplica a sus nodos secundarios.
 * Todos los tipos de entidades espaciales en Aspose.3D deben colocarse bajo una instancia de Nodo. Esto garantiza que los objetos como mallas, luces, cámaras y otros elementos se organizan dentro de la jerarquía de la escena.
 * Los nodos pueden contener varios materiales, y la relación entre los polígonos y los materiales adjuntos a un nodo se aborda utilizando el concepto `VertexElementMaterial` dentro del objeto Mesh.


¡! [Jerarquía de escena](scene.png)


## Entidades Espaciales
Todas las entidades espaciales dentro de Aspose.3D se heredan de la clase `Entity`, sirviendo como bloques de construcción fundamentales para construir entornos virtuales. Aspose.3D clasifica estas entidades en varias categorías principales, cada una con su propio propósito y funcionalidad específicos.

¡! [Entidades](entity.png)

* **Primitivo**La clase `Primitive` sirve como la clase base para todas las geometrías procedimentales 3D dentro de Aspose.3D, como `Cylinder`, `Torus` y `Sphere`. Estas geometrías se pueden definir utilizando un conjunto mínimo de parámetros, por lo que es conveniente crear formas 3D básicas.
* **Geometría**Las geometrías en Aspose.3D consisten típicamente en vértices, aristas y polígonos que definen la forma y estructura de un objeto 3D. Esta categoría abarca una amplia gama de geometrías complejas utilizadas para representar varios objetos dentro de una escena 3D.
* **Perfil**Los perfiles, similares a los primitivos, definen contornos cerrados 2D en el plano x-y. Proporcionamos una forma de crear formas 2D que se pueden extruir para generar las geometrías 3D correspondientes. Los perfiles se utilizan a menudo como punto de partida para crear objetos 3D más intrincados.
* **Curva**A diferencia de los perfiles, las curvas pueden estar abiertas o desconectadas. Se utilizan para definir rutas espaciales en 3D. Las curvas proporcionan un medio para crear rutas flexibles y personalizables que los objetos pueden seguir dentro de un entorno 3D.
* **Extrusión**Las extrusiones son una técnica de procedimiento empleada para construir geometrías 3D usando perfiles y curvas. Al aplicar extrusión a un perfil o una curva, se puede generar una forma 3D extendiendo el perfil o la curva a lo largo de una dirección especificada. Este enfoque permite la creación de geometrías más complejas y dinámicas.
* **Frustum**La categoría de frustum incluye objetos como luces y cámaras. Los frustos definen el volumen de visualización y la perspectiva en una escena 3D. Las cámaras utilizan frustums para determinar la parte de la escena que será visible, mientras que las luces utilizan frustums para definir la región dentro de la cual iluminan la escena.

Estas categorías principales de entidades en Aspose.3D abarcan una variedad de entidades que desempeñan papeles esenciales en la construcción y representación de entornos virtuales, proporcionando un conjunto de herramientas versátil para crear y manipular escenas 3D.


### Tipos de geometría

¡! [Tipos de geometría](geometries.png)

Aspose.3D contiene muchos tipos de geometría:


* `Mesh` Creación de malla de polígono amigable para herramientas.
* `PointCloud` Nube de puntos.
* `NurbsSurface` Superficies B-Spline racionales no uniformes.
* `Patch` Superficie definida por un conjunto de puntos de control y funciones de fusión.
* `TriMesh` Render API-malla basada en triángulo amigable.


Los más importantes de ellos son `Mesh` y `TriMesh`, las diferencias están en la tabla:

|Característica| `Mesh` | `TriMesh` |
| ---     |---     |---        |
|Polígono no-triángulo|Sí|No|
|Fácil de modificar|Sí|No|
|Reutilización del índice de datos|Sí|No|
|Cache CPU amigable|No|Sí|
|Rendering API amigable|No|Sí|
|Diseño de memoria fijo|No|Sí|

Las clases derivadas de `Geometry` están diseñadas para modificar y crear contenido, mientras que `TriMesh` está diseñado para representar.

Un `Geometry` consiste en puntos de control y `VertexElement` que definieron datos adicionales para el punto de control/borde/polígono/vértice de polígono, `Geometry` puede contener cero o más `VertexElement`, las subclases concretas `Geometry` implementaron diferentes métodos para modelar y representar geometrías 3D.


¡! [Tipos de geometría](mesh.png)


Puede crear manualmente un elemento de vértice y asignarle datos. El siguiente ejemplo de código muestra cómo hacer esto:

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

### Tipos de geometría primitiva


Aspose.3D proporciona un conjunto de tipos de geometría primitiva predefinidos que siguen reglas y algoritmos específicos para generar modelos 3D. Estos tipos primitivos simplifican el proceso de creación de geometrías 3D en comparación con el uso de tipos de geometría más complejos.

Los tipos primitivos predefinidos disponibles en Aspose.3D incluyen:

*  `Box`: La primitiva de caja permite crear formas cuboide rectangulares definidas por su anchura, altura y profundidad.
* Cilindro: con la primitiva de cilindro, puede generar formas cilíndricas especificando el radio y la altura. Esto es útil para crear objetos como tubos o columnas.
*  `Dish`: El plato primitivo permite la creación de geometrías en forma de plato, comúnmente utilizadas para representar objetos como cuencos o antenas parabólicas.
*  `Plane`: El plano primitivo genera superficies planas definidas por su anchura y longitud. Se utiliza con frecuencia como una base o plano de tierra en 3D escenas.
*  `Pyramid`: Con la primitiva de pirámide, puede crear geometrías piramidales caracterizadas por su tamaño de base y altura. Esto es útil para construir objetos como edificios o pirámides.
*  `Torus`: La primitiva de toro permite generar geometrías en forma de rosquilla con radios especificados para los círculos mayor y menor. Es adecuado para crear objetos que se asemejan a anillos o neumáticos.
*  `RectangularTorus`: La primitiva toro rectangular produce geometrías tipo toro con secciones transversales rectangulares en lugar de circulares. Proporciona flexibilidad adicional para crear formas únicas.
*  `Sphere`: La primitiva de esfera genera geometrías perfectamente redondas basadas en el radio especificado. Esto es útil para crear objetos como planetas o bolas.

Al utilizar estos tipos primitivos predefinidos en Aspose.3D, puede crear fácilmente una amplia gama de geometrías básicas 3D. Esto simplifica el proceso de modelado y le permite dar forma y ensamblar objetos rápidamente dentro de sus escenas 3D.

¡! [Tipos de geometría primitiva](primitives.png)

En el ejemplo de código siguiente se muestra cómo crear una esfera con el radio especificado:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java

        // initialize a scene
        Scene scene = new Scene();
        // initialize a Sphere
        Sphere sphere = new Sphere();
        // set radius
        sphere.setRadius(10);
        // add sphere to the scene
        scene.getRootNode().createChildNode(sphere);
        // save scene
        scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}


### Tipos de extrusión

La extrusión se puede usar para crear una variedad de objetos 3D complejos, es un método fundamental en el modelado 3D que implica extender un perfil 2D a lo largo de una curva para crear un objeto 3D.

En Aspose.3D hemos proporcionado 3 tipos de extrusión:

* `LinearExtrusion` La extrusión lineal toma un perfil 2D como entrada y extiende la forma en la tercera dimensión.
* `RevolvedAreaSolid` Esta clase representa un modelo sólido girando una sección transversal proporcionada por un perfil alrededor de un eje.
* `SweptAreaSolid` Esta clase representa un modelo sólido mediante un esquema de representación de barrido que permite que una sección transversal de perfil 2D barra a través del espacio.


¡! [Extrusiones](extrusions.png)

En el ejemplo de código siguiente se muestra cómo crear una extrusión lineal a partir de un perfil de texto:

{{< highlight "java" >}}
    // Load font from bytes
    var font = FontFile.parse(Files.readAllBytes(Paths.get("test-font.otf")));
    // Create a Text profile
    var text = new Text();
    text.setFont(font);
    text.setContent("Hello World");
    text.setFontSize(10.0f);
    // Extrude the profile to give it a thickness.
    var linear = new LinearExtrusion(text, 10).toMesh();
    // create a scene from the mesh and save it to stl file
    var scene = new Scene(linear);
    scene.save("test.stl");


{{< /highlight >}}


### Tipos de curva

En Aspose.3D, una curva representa una o más trayectorias espaciales que pueden tomar varias formas, como líneas, curvas NURBS o curvas compuestas por múltiples segmentos de curva. Las curvas se suelen utilizar junto con los tipos de extrusión para crear formas 3D dinámicas e intrincadas.

Las curvas se pueden emplear para definir rutas complejas que los objetos siguen dentro de un entorno 3D, lo que permite movimientos suaves y precisos. Al utilizar diferentes tipos de curvas y componerlas juntas, puede lograr rutas espaciales versátiles y personalizables para sus modelos 3D.

Además, ciertos formatos de archivo soportados por Aspose.3D también proporcionan la capacidad de importar y exportar datos de curva. Esto le permite integrar sin problemas curvas creadas en aplicaciones externas o compartir curvas generadas dentro de Aspose.3D con otro software.


¡! [Tipos de curva](curves.png)

## Tipos de perfil

Aspose.3D ofrece una gama de perfiles 2D que se pueden utilizar para crear formas o contornos cerrados dentro de un entorno 3D. Estos perfiles permiten la creación de estructuras 2D intrincadas que se pueden extruir o manipular en geometrías 3D. Aquí hay algunas implementaciones de perfil notables en Aspose.3D:

* `ParameterizedProfile`: Aspose.3D proporciona varias implementaciones que ofrecen perfiles con formas estándar. Estos perfiles predefinidos permiten la creación rápida de formas de uso común, como círculos, rectángulos y polígonos.

* `MirroredProfile`: Este tipo de perfil le permite reflejar un perfil existente a lo largo del eje Y, creando una forma simétrica. Proporciona una forma conveniente de generar perfiles equilibrados y visualmente atractivos.

* `ArbitraryProfile`: Con la implementación de perfil arbitrario, puede asignar una curva arbitraria para crear un perfil cerrado. Esto ofrece flexibilidad en el diseño de formas personalizadas mediante la definición de una curva y su conversión en un perfil cerrado para su posterior manipulación.

* `Text`: Aspose.3D incluye la capacidad de generar perfiles a partir de texto utilizando una fuente especificada. Esta función le permite crear perfiles en forma de letras, números o cualquier otro contenido textual, agregando un elemento de personalización o marca a sus modelos 3D.

¡! [Tipos de perfil 2D](profiles.png)

### Cámara y tipos de luz

¡! [Cámara y luz](frustums.png)

## Tipos de material

Aspose.3D proporciona soporte para varios tipos de materiales, incluyendo material Lambert, material Phong, material PBR, material PBR especular y material de sombreado (sólo disponible en archivos FBX).

Cada material en Aspose.3D puede tener diferentes atributos y propiedades que definen su apariencia y comportamiento dentro de una escena 3D. Estos materiales se pueden conectar a instancias de textura, mejorando sus características visuales.

Las texturas en Aspose.3D están asociadas con un atributo de material específico. El tipo de textura combina las definiciones de parámetros para el origen de imagen y el muestreador de textura. Al utilizar texturas, puede aplicar patrones detallados, colores y otros efectos visuales a las superficies de sus modelos 3D.

Con el soporte para una variedad de tipos de materiales y la capacidad de conectar texturas, Aspose.3D ofrece flexibilidad para crear materiales visualmente atractivos y realistas para sus escenas 3D.

¡! [Tipos de material](materials.png)

El ejemplo de código siguiente muestra cómo aplicar un material PBR a una geometría:

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

## Relación de objetos de animación
Aspose.3D proporciona soporte de animación a nivel de datos, y el soporte de cálculo se está desarrollando actualmente.

En Aspose.3D, una escena puede contener varios objetos AnimationClip. Cada clip de animación puede constar de varios nodos de animación. El nodo de animación sigue el patrón de diseño compuesto, lo que permite la creación de estructuras jerárquicas con nodos de subanimación.

Los nodos de animación se pueden asociar a puntos de enlace, que definen las propiedades del objeto de destino que se animará. Los vectores son tipos de datos de uso común en muchas propiedades de entidad. Por lo tanto, los puntos de enlace pueden tener diferentes canales de animación para actualizar canales específicos del vector independientemente. Cada canal contiene una secuencia de fotogramas clave que define cómo se anima el valor a lo largo del tiempo.

Este sistema proporciona un marco flexible para animar objetos dentro de una escena. Al definir clips de animación, nodos, puntos de enlace y canales, puede crear animaciones complejas y dinámicas que afectan a varias propiedades de las entidades de la escena 3D.

Mientras que Aspose.3D actualmente admite animación a nivel de datos, el desarrollo en curso se centra en la expansión del soporte de cálculo, lo que mejorará las capacidades para crear y manipular animaciones dentro del marco.

¡! [Animaciones](animations.png)


Una escena con animaciones puede tener este tipo de estructura:


¡! [Muestra de animaciones](animation_relations.png)