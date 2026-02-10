---
title: Ajout de la transformation au nœud
type: docs
weight: 10
url: /fr/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API a le support pour faire pivoter les objets dans l'espace 3D. Il existe trois façons de définir la rotation de l'objet dans l'espace 3D, les angles d'Euler, le quaternion et la matrice personnalisée, toutes sont supportées par la classe Transform.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API a le support pour faire pivoter les objets dans l'espace 3D. Il y a trois façons de définir la rotation de l'objet dans l'espace 3D, les angles d'Euler, Quaternion et Custom Matrix, toutes sont supportées par la classe `Transform`.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) sont les plus couramment utilisés dans le scénario 3D, nous avons fourni une classe `Transform` pour y accéder dans Aspose.3D Les transformations affines incluent:

- Traduction
- Mise à l'échelle
- Rotation
- Cartographie de cisaillement
- Cartographie à presser

{{% alert color="primary" %}} 

L'objet de classe `Mesh` est utilisé dans le code. Nous pouvons [Créer un objet de classe Mesh tel que raconté là-bas](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
##  **Tourner par Quaternion**
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
##  **Tourner par Euler Angles**
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
##  **Matrice de transformation personnalisée**
Nous pouvons également utiliser Matrix directement:

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
