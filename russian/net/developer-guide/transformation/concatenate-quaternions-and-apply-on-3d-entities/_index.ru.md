---
title: Сплетите кватернионы и примените их к лицам 3D
type: docs
weight: 50
url: /ru/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET позволяет разработчикам объединить два преобразования ротации в одно, представленное в кватернионе.
---
{{% alert color="primary" %}} 

[Aspose.3D for .NET](https://www.aspose.com/products/3d) позволяет разработчикам объединить два преобразования ротации в одно, представленное в кватернионе.

{{% /alert %}} 
##  **Конкатенатные кватернионы**
Кватернионы используются для представления ориентации в пространстве 3D. Метод `Concat`, представленный классом [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion), можно использовать для объединения двух кватернионов. В этом примере кода мы объединяем два кватерниона и получаем третий полученный кватернион, а затем применяем эти три кватерниона к трем цилиндрам.
###  **Образец программирования**
Этот пример кода объединяет два кватерниона и применяет их к разным цилиндрам.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            Scene scene = new Scene();

            Quaternion q1 = Quaternion.FromEulerAngle(Math.PI * 0.5, 0, 0);
            Quaternion q2 = Quaternion.FromAngleAxis(-Math.PI * 0.5, Vector3.XAxis);
            // Concatenate q1 and q2. q1 and q2 rotate alone x-axis with same angle but different direction,
            // So the concatenated result will be identity quaternion.
            Quaternion q3 = q1.Concat(q2);

            // Create 3 cylinders to represent each quaternion
            Node cylinder = scene.RootNode.CreateChildNode("cylinder-q1", new Cylinder(0.1, 1, 2));
            cylinder.Transform.Rotation = q1;
            cylinder.Transform.Translation = new Vector3(-5, 2, 0);

            cylinder = scene.RootNode.CreateChildNode("cylinder-q2", new Cylinder(0.1, 1, 2));
            cylinder.Transform.Rotation = q2;
            cylinder.Transform.Translation = new Vector3(0, 2, 0);

            cylinder = scene.RootNode.CreateChildNode("cylinder-q3", new Cylinder(0.1, 1, 2));
            cylinder.Transform.Rotation = q3;
            cylinder.Transform.Translation = new Vector3(5, 2, 0);
            // Save to file
            scene.Save("test_out.fbx");

{{< /highlight >}}


**Результат в 3ds MAX**

! [Для: имаге_альт_текст](concatenate-quaternions-and-apply-on-3d-entities_1.png)
