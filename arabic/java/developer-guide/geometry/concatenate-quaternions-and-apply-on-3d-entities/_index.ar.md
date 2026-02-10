---
title: رباعيات متسلسلة وتقدم الطلب على كيانات 3D
type: docs
weight: 30
url: /ar/java/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Java يسمح للمطورين بدمج تحولي دوران إلى تحويل واحد ممثل في رباعي.
---
{{% alert color="primary" %}} 

Aspose.3D for Java يسمح للمطورين بدمج تحولي دوران إلى تحويل واحد ممثل في رباعي.

{{% /alert %}} 
##  **Concatenate uuaternions**
تُستخدم كواتيرنيون لتمثيل اتجاه في مساحة 3D. يمكن استخدام طريقة concat التي تعرضها فئة `Quaternion` للجمع بين اثنين من quaternions. في هذا المثال البرمجي ، ندمج اثنين من رباعي الأيونات ونحصل على رباعي ثالث ناتج ، ثم نطبق هذه الرباعي الثلاثة على ثلاث أسطوانات.
###  **Pروغرامينغ ple وافرة**
Tله رمز المثال الجمع بين اثنين من رباتيرفيونس وتطبيقها على اسطوانات مختلفة.

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




**Result في 3ds MAX**

! [Todo: image_ altttext](concatenate-quaternions-and-apply-on-3d-entities_1.png)
