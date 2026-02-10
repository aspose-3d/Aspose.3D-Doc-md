---
title: Arbeiten mit Zylinder
type: docs
weight: 130
url: /de/net/working-with-cylinder/
description: Aspose.3D for .NET ermöglicht das Anpassen von Offset-Oberteil eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die Offset-Eigenschaft der Cylinder-Klasse verwenden.
---
#  **Offset-Top anpassen**
Aspose.3D for .NET ermöglicht das Anpassen von Offset-Oberteil eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `Offset` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Offset Top angepasst wird:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a scene
Scene scene = new Scene();
// Initialize cylinder
var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Set OffsetTop
cylinder1.OffsetTop = new Vector3(5, 3, 0);
// Create ChildNode
scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);
// Intialze second cylinder without customized OffsetTop
var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Create ChildNode
scene.RootNode.CreateChildNode(cylinder2);
// Save
scene.Save("CustomizedOffsetTopCylinder.obj");

{{< /highlight >}}

! [Todo: image_alt_text](working-with-cylinder_1.png)

Im linken ist OffsetTop auf (5, 3, 0) eingestellt. Es ist leicht zu erkennen, dass sich die obere Kappe bewegt hat und auch der gesamte Torso betroffen ist.
#  **Shear Bottom anpassen**
Aspose.3D for .NET ermöglicht die Anpassung des Scher bodens eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `ShearBottom` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Shear Bottom angepasst wird:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a scene
Scene scene = new Scene();
// Create cylinder 1
var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Customized shear bottom for cylinder 1
cylinder1.ShearBottom = new Vector2(0, 0.83);// shear 47.5deg in xy plane(z-axis)
// Add cylinder 1 to the scene
scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);
// Create cylinder 2
var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Add cylinder to without a ShearBottom to the scene
scene.RootNode.CreateChildNode(cylinder2);
// Save scene
scene.Save("CustomizedShearBottomCylinder.obj");


{{< /highlight >}}

! [Todo: image_alt_text](working-with-cylinder_2.png)

Der linke Zylinder hat `ShearBottom` bis (0, 0.83), während der rechte ein Ordnungszylinder ist.
#  **Lüfter zylinder erstellen**
Aspose.3D for .NET ermöglicht die Erstellung eines Lüfter zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `GenerateFanCylinder` der Klasse `Cylinder` auf `true` festlegen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a scene
Scene scene = new Scene();
// Create cylinder 1
var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
// Customized shear bottom for cylinder 1
cylinder1.ShearBottom = new Vector2(0, 0.83);// shear 47.5deg in xy plane(z-axis)
// Add cylinder 1 to the scene
scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);
// Create cylinder 2
var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
// Add cylinder to without a ShearBottom to the scene
scene.RootNode.CreateChildNode(cylinder2);
// Save scene
scene.Save("CustomizedShearBottomCylinder.obj");


{{< /highlight >}}

! [Todo: image_alt_text](working-with-cylinder_3.png)

Der linke Zylinder hat `GenerateFanCylinder = false` und der rechte hat `GenerateFanCylinder = true`.
