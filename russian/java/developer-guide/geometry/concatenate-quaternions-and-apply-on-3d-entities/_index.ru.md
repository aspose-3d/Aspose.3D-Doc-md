---
title: Сплетите кватернионы и примените их к лицам 3D
type: docs
weight: 30
url: /ru/java/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Java позволяет разработчикам объединить два преобразования ротации в одно, представленное в кватернионе.
---
{{% alert color="primary" %}} 

Aspose.3D for Java позволяет разработчикам объединить два преобразования ротации в одно, представленное в кватернионе.

{{% /alert %}} 
##  **Конкатенатные кватернионы**
Кватернионы используются для представления ориентации в пространстве 3D. Метод concat, представленный классом `Quaternion`, может быть использован для объединения двух кватернионов. В этом примере кода мы объединяем два кватерниона и получаем третий полученный кватернион, а затем применяем эти три кватерниона к трем цилиндрам.
###  **Образец программирования**
Этот пример кода объединяет два кватерниона и применяет их к разным цилиндрам.

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




**Результат в 3ds MAX**

! [Для: имаге_альт_текст](concatenate-quaternions-and-apply-on-3d-entities_1.png)
