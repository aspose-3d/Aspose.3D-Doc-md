---
title: Adding Transformation to the Node
type: docs
weight: 10
url: /java/adding-transformation-to-the-node/
description: Aspose.3D for Java API has support to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the Transform class.
---

{{% alert color="primary" %}} 

Aspose.3D for Java API has support to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the `Transform` class.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class `Transform` to access these in Aspose.3D Affine transformations include:

- Translation
- Scaling
- Rotation
- Shear mapping
- Squeeze mapping

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Rotate by Quaternion**
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
## **Rotate by Euler Angles**
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
## **Custom Transformation Matrix**
We can also use Matrix directly:

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
