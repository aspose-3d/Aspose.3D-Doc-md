---
title: Concatenate Quaternions and apply on 3D entities
type: docs
weight: 30
url: /tr/java/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Java, geliştiricilerin bir kuaternionda temsil edilen iki rotasyon dönüşümünü birleştirmelerine izin verir.
---
{{% alert color="primary" %}} 

Aspose.3D for Java, geliştiricilerin bir kuaternionda temsil edilen iki rotasyon dönüşümünü birleştirmelerine izin verir.

{{% /alert %}} 
##  **Concatenate Quaternions**
Quaternions are used to represent an orientation in 3D space. The concat method exposed by the `Quaternion` class can be used to combine two quaternions. In this code example, we combine two quaternions and get a third resulting quaternion, and then apply these three quaternions to three cylinders.
###  **Programming ample ample**
Kod örneği iki kuaternionu birleştirir ve bunları farklı silindirlere uygular.

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




**3ds MAX esuesuesuesu**

! [Todo: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
