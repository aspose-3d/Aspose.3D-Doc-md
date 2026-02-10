---
title: Concaténer les quaternions et appliquer sur les entités 3D
type: docs
weight: 50
url: /fr/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET permet aux développeurs de combiner deux transformations de rotation en une seule représentée dans un quaternion.
---
{{% alert color="primary" %}} 

[Aspose.3D for .NET](https://www.aspose.com/products/3d) permet aux développeurs de combiner deux transformation de rotation en une seule représentée dans un quaternion.

{{% /alert %}} 
##  **Quaternions concaténer**
Les quaternions sont utilisés pour représenter une orientation dans l'espace 3D. La méthode `Concat` exposée par la classe [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) peut être utilisée pour combiner deux quaternions. Dans cet exemple de code, nous combinons deux quaternions et obtenons un troisième quaternion résultant, puis nous appliquons ces trois quaternions à trois cylindres.
###  **Échantillon de programmation**
Cet exemple de code combine deux quaternions et les applique à différents cylindres.

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


**Résultat dans 3ds MAX**

! [Tout le monde: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
