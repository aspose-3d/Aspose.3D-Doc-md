---
title: Concaténer les quaternions et appliquer sur les entités 3D
type: docs
weight: 30
url: /fr/java/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Java permet aux développeurs de combiner deux transformations de rotation en une seule représentée dans un quaternion.
---
{{% alert color="primary" %}} 

Aspose.3D for Java permet aux développeurs de combiner deux transformations de rotation en une seule représentée dans un quaternion.

{{% /alert %}} 
##  **Quaternions concaténer**
Les quaternions sont utilisés pour représenter une orientation dans l'espace 3D. La méthode concat exposée par la classe `Quaternion` peut être utilisée pour combiner deux quaternions. Dans cet exemple de code, nous combinons deux quaternions et obtenons un troisième quaternion résultant, puis nous appliquons ces trois quaternions à trois cylindres.
###  **Échantillon de programmation**
Cet exemple de code combine deux quaternions et les applique à différents cylindres.

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




**Résultat dans 3ds MAX**

! [Tout le monde: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
