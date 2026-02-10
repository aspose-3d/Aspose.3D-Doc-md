---
title: رباعيات متسلسلة وتقدم الطلب على كيانات 3D
type: docs
weight: 50
url: /ar/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET يسمح للمطورين بدمج تحولي دوران إلى تحويل واحد ممثل في رباعي.
---
{{% alert color="primary" %}} 

يسمح [Aspose.3D for .NET](https://www.aspose.com/products/3d) للمطورين بدمج تحولي دوران إلى تحويل واحد ممثل في رباعي.

{{% /alert %}} 
##  **Concatenate uuaternions**
تُستخدم كواتيرنيون لتمثيل اتجاه في مساحة 3D. يمكن استخدام طريقة `Concat` المعروضة بواسطة فئة [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) للجمع بين رباعي. في هذا المثال البرمجي ، ندمج اثنين من رباعي الأيونات ونحصل على رباعي ثالث ناتج ، ثم نطبق هذه الرباعي الثلاثة على ثلاث أسطوانات.
###  **Pروغرامينغ ple وافرة**
Tله رمز المثال الجمع بين اثنين من رباتيرفيونس وتطبيقها على اسطوانات مختلفة.

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


**Result في 3ds MAX**

! [Todo: image_ altttext](concatenate-quaternions-and-apply-on-3d-entities_1.png)
