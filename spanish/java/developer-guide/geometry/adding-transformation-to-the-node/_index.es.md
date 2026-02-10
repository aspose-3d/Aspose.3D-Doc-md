---
title: Adición de transformación al nodo
type: docs
weight: 10
url: /es/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API tiene soporte para rotar objetos en el espacio 3D. Hay tres formas de definir la rotación del objeto en el espacio 3D, los ángulos de Euler, Quaternion y Custom Matrix, todos ellos son compatibles con la clase Transform.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte para rotar objetos en el espacio 3D. Hay tres formas de definir la rotación de un objeto en el espacio 3D, los ángulos de Euler, Quaternion y Custom Matrix, todos ellos son compatibles con la clase `Transform`.

{{% /alert %}} 

TSR (Traducción/Escala/Rotación) se usan más comúnmente en el escenario 3D, proporcionamos una clase `Transform` para acceder a estos en Aspose.3D Las transformaciones afín incluyen:

- Traducción
- Escala
- Rotación
- Mapeo de cizalla
- Mapeo de apretar

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
##  **Girar por el cuaternión**
{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the Mesh geometry
cubeNode.setEntity(mesh);
// Set rotation
cubeNode.getTransform().setRotation(Quaternion.fromRotation(new Vector3(0, 1, 0), new Vector3(0.3, 0.5, 0.1)));
// Set translation
cubeNode.getTransform().setTranslation(new Vector3(0, 0, 20));
// Add cube to the scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("TransformationToNode.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Girar por ángulos de Euler**
{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the Mesh geometry
cubeNode.setEntity(mesh);
// Euler angles
cubeNode.getTransform().setEulerAngles(new Vector3(0.3, 0.1, -0.5));
// Set translation
cubeNode.getTransform().setTranslation(new Vector3(0, 0, 20));
// Add cube to the scene
scene.getRootNode().getChildNodes().add(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("TransformationToNode.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
##  **Matriz de transformación personalizada**
También podemos utilizar la matriz directamente:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize Node class object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the Mesh geometry
cubeNode.setEntity(mesh);
// Set custom translation matrix
cubeNode.getTransform().setTransformMatrix(new Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));
// Add cube to the scene
scene.getRootNode().addChildNode(cubeNode);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("TransformationToNode.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
