---
title: Quaternionen verkettieren und auf 3D Entitäten anwenden
type: docs
weight: 50
url: /de/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET ermöglicht es Entwicklern, zwei Rotations transformationen zu einer in einer Quaternion dargestellten zu kombinieren.
---
{{% alert color="primary" %}} 

Mit [Aspose.3D for .NET](https://www.aspose.com/products/3d) können Entwickler zwei Rotations transformationen zu einer in einer Quaternion dargestellten kombinieren.

{{% /alert %}} 
##  **Quaternionen verkettieren**
Quaternionen werden verwendet, um eine Orientierung im Raum 3D darzustellen. Die `Concat`-Methode der [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion)-Klasse kann verwendet werden, um zwei Quaternionen zu kombinieren. In diesem Code beispiel kombinieren wir zwei Quaternionen und erhalten eine dritte resultierende Quaternion. Anschließend wenden wir diese drei Quaternionen auf drei Zylinder an.
###  **Programmier probe**
Dieses Code beispiel kombiniert zwei Quaternionen und wendet sie auf verschiedene Zylinder an.

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


**Ergebnis in 3ds MAX**

! [Todo: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
