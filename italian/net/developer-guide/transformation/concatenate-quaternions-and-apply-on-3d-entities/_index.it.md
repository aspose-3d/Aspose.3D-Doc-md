---
title: Concatenare i quaternioni e applicare su 3D entità
type: docs
weight: 50
url: /it/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET consente agli sviluppatori di combinare due trasformazioni di rotazione in una rappresentata in un quaternione.
---
{{% alert color="primary" %}} 

[Aspose.3D for .NET](https://www.aspose.com/products/3d) consente agli sviluppatori di combinare due trasformazioni di rotazione in una rappresentata in un quaternione.

{{% /alert %}} 
##  **Concatenati quaternioni**
I quaternioni vengono utilizzati per rappresentare un orientamento nello spazio 3D. Il metodo `Concat` esposto dalla classe [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) può essere utilizzato per combinare due quaternioni. In questo esempio di codice, combiniamo due quaternioni e otteniamo un terzo quaternione risultante, quindi applichiamo questi tre quaternioni a tre cilindri.
###  **Campione di programmazione**
Questo esempio di codice combina due quaternioni e li applica a diversi cilindri.

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


**Risultato in 3ds MAX**

! [Todo: image_alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
