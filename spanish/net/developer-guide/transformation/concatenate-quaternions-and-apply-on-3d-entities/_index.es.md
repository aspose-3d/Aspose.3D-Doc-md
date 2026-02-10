---
title: Concatenar cuaterniones y aplicar en entidades 3D
type: docs
weight: 50
url: /es/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET permite a los desarrolladores combinar dos transformaciones de rotación en una representada en un cuaternión.
---
{{% alert color="primary" %}} 

[Aspose.3D for .NET](https://www.aspose.com/products/3d) permite a los desarrolladores combinar dos transformaciones de rotación en una representada en un cuaternión.

{{% /alert %}} 
##  **Concatenar cuaterniones**
Los cuaterniones se usan para representar una orientación en el espacio 3D. El método `Concat` expuesto por la clase [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) se puede usar para combinar dos cuaterniones. En este ejemplo de código, combinamos dos cuaterniones y obtenemos un tercer cuaterniones resultante, y luego aplicamos estos tres cuaterniones a tres cilindros.
###  **Muestra de programación**
Este ejemplo de código combina dos cuaterniones y los aplica a diferentes cilindros.

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


**Resultado en 3ds MAX**

¡! [Todo: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
