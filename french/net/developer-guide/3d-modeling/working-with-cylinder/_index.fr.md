---
title: Travailler avec le cylindre
type: docs
weight: 130
url: /fr/net/working-with-cylinder/
description: Aspose.3D for .NET permet de personnaliser le haut décalé d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété Offset de la classe Cylinder.
---
#  **Personnaliser le haut offset**
Aspose.3D for .NET permet de personnaliser le haut décalé d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété `Offset` de la classe `Cylinder`. L'extrait de code suivant montre comment personnaliser Offset Top:



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

! [Tout le monde: image_alt_text](working-with-cylinder_1.png)

Celui de gauche a OffsetTop réglé sur (5, 3, 0), il est facile de voir que la casquette supérieure a bougé et que tout le torse est également affecté.
#  **Personnaliser ShearBottom**
Aspose.3D for .NET permet de personnaliser le fond de cisaillement d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété `ShearBottom` de la classe `Cylinder`. L'extrait de code suivant montre comment personnaliser Shear Bottom:



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

! [Tout le monde: image_alt_text](working-with-cylinder_2.png)

Le cylindre de gauche a `ShearBottom` à (0, 0.83) tandis que celui de droite est un cylindre ordinal.
#  **Créer un ventilateur-cylindre**
Aspose.3D for .NET permet de créer un cylindre de ventilateur. Pour utiliser cette fonctionnalité, vous pouvez définir la propriété `GenerateFanCylinder` de la classe `Cylinder` à `true`. L'extrait de code suivant montre comment utiliser cette fonctionnalité:



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

! [Tout le monde: image_alt_text](working-with-cylinder_3.png)

Le cylindre de gauche a `GenerateFanCylinder = false` et le droit a `GenerateFanCylinder = true`.
