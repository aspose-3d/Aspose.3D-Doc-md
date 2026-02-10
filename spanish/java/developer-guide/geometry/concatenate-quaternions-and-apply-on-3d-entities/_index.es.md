---
title: Concatenar cuaterniones y aplicar en entidades 3D
type: docs
weight: 30
url: /es/java/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Java permite a los desarrolladores combinar dos transformaciones de rotación en una representada en un cuaternión.
---
{{% alert color="primary" %}} 

Aspose.3D for Java permite a los desarrolladores combinar dos transformaciones de rotación en una representada en un cuaternión.

{{% /alert %}} 
##  **Concatenar cuaterniones**
Los cuaterniones se usan para representar una orientación en el espacio 3D. El método concat expuesto por la clase `Quaternion` se puede usar para combinar dos cuaterniones. En este ejemplo de código, combinamos dos cuaterniones y obtenemos un tercer cuaterniones resultante, y luego aplicamos estos tres cuaterniones a tres cilindros.
###  **Muestra de programación**
Este ejemplo de código combina dos cuaterniones y los aplica a diferentes cilindros.

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




**Resultado en 3ds MAX**

¡! [Todo: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
