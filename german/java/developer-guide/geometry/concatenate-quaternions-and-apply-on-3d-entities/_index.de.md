---
title: Quaternionen verkettieren und auf 3D Entitäten anwenden
type: docs
weight: 30
url: /de/java/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Java ermöglicht es Entwicklern, zwei Rotations transformationen zu einer in einer Quaternion dargestellten zu kombinieren.
---
{{% alert color="primary" %}} 

Aspose.3D for Java ermöglicht es Entwicklern, zwei Rotations transformationen zu einer in einer Quaternion dargestellten zu kombinieren.

{{% /alert %}} 
##  **Quaternionen verkettieren**
Quaternionen werden verwendet, um eine Orientierung im Raum 3D darzustellen. Die von der `Quaternion`-Klasse exponierte Concat-Methode kann verwendet werden, um zwei Quaternionen zu kombinieren. In diesem Code beispiel kombinieren wir zwei Quaternionen und erhalten eine dritte resultierende Quaternion. Anschließend wenden wir diese drei Quaternionen auf drei Zylinder an.
###  **Programmier probe**
Dieses Code beispiel kombiniert zwei Quaternionen und wendet sie auf verschiedene Zylinder an.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
Scene scene = new Scene();
Quaternion q1 = Quaternion.fromEulerAngle(Math.PI * 0.5, 0, 0);
Vector3.X_AXIS.x = 3;
Quaternion q2 = Quaternion.fromAngleAxis(-Math.PI * 0.5, Vector3.X_AXIS);
// Concatenate q1 and q2. q1 and q2 rotate alone x-axis with same angle but different direction,
// So the concatenated result will be identity quaternion.
Quaternion q3 = q1.concat(q2);
// Create 3 cylinders to represent each quaternion
Node cylinder = scene.getRootNode().createChildNode("cylinder-q1", new Cylinder(0.1, 1, 2));
cylinder.getTransform().setRotation(q1);
cylinder.getTransform().setTranslation(new Vector3(-5, 2, 0));
cylinder = scene.getRootNode().createChildNode("cylinder-q2", new Cylinder(0.1, 1, 2));
cylinder.getTransform().setRotation(q2);
cylinder.getTransform().setTranslation(new Vector3(0, 2, 0));
cylinder = scene.getRootNode().createChildNode("cylinder-q3", new Cylinder(0.1, 1, 2));
cylinder.getTransform().setRotation(q3);
cylinder.getTransform().setTranslation(new Vector3(5, 2, 0));
MyDir = MyDir + "test_out.fbx";
// Save to file
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}




**Ergebnis in 3ds MAX**

! [Todo: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
