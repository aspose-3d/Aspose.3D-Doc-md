---
title: Aggiunta della trasformazione al nodo
type: docs
weight: 10
url: /it/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API supporta la rotazione degli oggetti nello spazio 3D. Esistono tre modi per definire la rotazione dell'oggetto nello spazio 3D, angoli di Eulero, Quaternion e Custom Matrix, tutti supportati dalla classe Transform.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporta la rotazione degli oggetti nello spazio 3D. Esistono tre modi per definire la rotazione dell'oggetto nello spazio 3D, angoli di Eulero, Quaternion e Custom Matrix, tutti supportati dalla classe `Transform`.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) sono più comunemente utilizzati nello scenario 3D, abbiamo fornito una classe `Transform` per accedere a questi in Aspose.3D Le trasformazioni affini includono:

- Traduzione
- Scalatura
- Rotazione
- Mappatura del taglio
- Spremi la mappatura

{{% alert color="primary" %}} 

L'oggetto della classe `Mesh` viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
##  **Ruota da Quaternion**
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
##  **Ruota per angoli di Eulero**
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
##  **Matrice di trasformazione personalizzata**
Possiamo anche usare Matrix direttamente:

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
