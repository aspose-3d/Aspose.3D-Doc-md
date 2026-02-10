---
title: Konstatera Quaternions och sök på 3D-titeter
type: docs
weight: 50
url: /sv/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET tillåter utvecklare att kombinera två rotationsomvandlingar till en som representeras i en quaternion.
---
{{% alert color="primary" %}} 

[Aspose.3D for .NET](https://www.aspose.com/products/3d) låter utvecklare kombinera två rotationsomvandlingar till en som representeras i en quaternion.

{{% /alert %}} 
##  **Konkreta kvitteringar**
Quaternions används för att representera en orientering i 3D mellanslag. `Concat`-metoden som exponeras av [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion)-klassen kan användas för att kombinera två quaternioner. I detta kodexempel, kombinerar vi två quaternions och får en tredje resulterande quaternion, och sedan tillämpa dessa tre quaternioner till tre cylindrar.
###  **Programmeringsprova**
Detta kodexempel kombinerar två quaternioner och applicera dem på olika cylindrar.

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


**Resultat i 3ds MAX**

![todo:image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
