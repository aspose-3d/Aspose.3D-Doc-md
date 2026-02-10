---
title: Convertir malla a malla de triángulo y forma primitiva a malla
type: docs
weight: 20
url: /es/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API tiene soporte para convertir malla a malla triangular con diseño de memoria personalizado del vértice. El diseño de memoria personalizado de Vertex se define dinámicamente por la clase VertexDeclaration en los ejemplos de código.
---
##  **Convertir malla a malla triangular con diseño de memoria personalizado de vértice**
Aspose.3D for Java API tiene soporte para convertir malla a malla triangular con diseño de memoria personalizado del vértice. El diseño de memoria personalizado de Vertex se define dinámicamente por la clase `VertexDeclaration` en los ejemplos de código.

{{% alert color="primary" %}}

Este tema de ayuda crea mallas de la caja y la esfera para mantener el código completo y corto. Los desarrolladores pueden construir una malla manualmente como se narra en este tema de ayuda: [Crear malla de cubo 3D](/3d/es/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Los desarrolladores pueden convertir malla en malla triangular porque cualquier estructura compleja (de superficie) se puede representar como un montón de triángulos. El triángulo es la geometría más atómica. Así se utiliza como base para casi cualquier cosa. Este ejemplo de código convierte una malla Box en triángulo con diseño de memoria personalizado.



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
##  **Convertir forma primitiva a malla**
Aspose.3D for Java API tiene soporte para convertir cualquier forma primitiva en malla. Las formas primitivas incluyen objetos más básicos y usados como caja, esfera, plano, cilindro y toro.

{{% alert color="primary" %}}

Cualquier clase que implemente una interfaz IMeshConvertible se puede convertir en malla mientras se exporta a cualquier formato de archivo 3D.

{{% /alert %}}
###  **Convertir Esfera primitiva a Malla**
Una esfera es un objeto geométrico perfectamente redondo en un espacio tridimensional que aparece en todas partes, desde balones deportivos hasta planetas en el espacio. Usemos la Esfera primitiva para crear una malla.
El ejemplo de código a continuación convierte una esfera en malla.

{{< highlight "java" >}}
// Initialize object by Sphere class
IMeshConvertible convertible = new Sphere();
// Convert a Sphere to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir caja a malla**
Una caja describe una variedad de contenedores y receptáculos para uso permanente como almacenamiento, o para uso temporal, a menudo para transportar contenido. Usemos la caja primitiva para crear una malla. El ejemplo de código a continuación convierte un Box en malla.

{{< highlight "java" >}}
// Initialize object by Box class
IMeshConvertible convertible = new Box();
// Convert a Box to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir un avión a malla**
Un plano se extiende infinitamente sin espesor. Un ejemplo de un plano es un plano de coordenadas. Permite utilizar la primitiva Plano para crear una malla. El siguiente ejemplo de código convierte un plano a malla.

{{< highlight "java" >}}
// Initialize object by Plane class
IMeshConvertible convertible = new Plane();
// Convert a Plane to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir un cilindro a malla**
Un cilindro es una de las formas geométricas curvilíneas más básicas, la superficie formada por los puntos a una distancia fija de una línea recta dada, el eje del cilindro. Se puede utilizar en muchos lugares, por ejemplo, como pilar frente a una casa o como eje de transmisión de automóviles. Permite usar el cilindro primitivo para crear una malla. El ejemplo de código a continuación convierte un cilindro en malla.

{{< highlight "java" >}}
// Initialize object by Cylinder class
IMeshConvertible convertible = new Cylinder();
// Convert a Cylinder to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
###  **Convertir un torus a malla**
Un toro es una superficie de revolución generada al girar un círculo en un espacio tridimensional alrededor de un eje coplanar con el círculo. Si el eje de revolución no toca el círculo, la superficie tiene forma de anillo y se llama toro de revolución. Usemos el primitivo Torus para crear una malla. El siguiente ejemplo de código convierte un Torus a malla.

{{< highlight "java" >}}
// Initialize object by Torus class
IMeshConvertible convertible = new Torus();
// Convert a Torus to Mesh
Mesh mesh = convertible.toMesh();
{{< /highlight >}}
