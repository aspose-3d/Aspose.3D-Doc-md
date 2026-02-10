---
title: Arbeta med cylinder
type: docs
weight: 130
url: /sv/net/working-with-cylinder/
description: Aspose.3D for .NET tillåter anpassning av offset Topp i en cylinder. För att använda denna funktionalitet kan du använda Offset egenskap av Cylinderklass.
---
#  **Anpassa offset övrev**
Aspose.3D for .NET tillåter anpassning av offset Topp i en cylinder. För att kunna använda denna funktionalitet, kan du använda `Offset` egenskapen i `Cylinder` klassen. Följande kod snutt visar hur man anpassar Offset Top:



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

![todo:image_alt_text](working-with-cylinder_1.png)

Den vänstra har OffsetTop satt till (5, 3, 0), Det är lätt att se att topplocket har flyttat och hela bålet påverkas också.
#  **Anpassa shearBottom**
Aspose.3D for .NET tillåter anpassning av skjuvningsbotten på en cylinder. För att kunna använda denna funktionalitet, kan du använda `ShearBottom` egenskapen i `Cylinder` klassen. Följande kodutdrag visar hur man anpassar skjuv nedre:



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

![todo:image_alt_text](working-with-cylinder_2.png)

Den vänstra cylindern har `ShearBottom` till (0, 0.83) medan den högra är en ordinarie cylinder.
#  **Skapa fläkt- cylinder**
Aspose.3D for .NET tillåter skapandet av en fläktcylinder. För att kunna använda denna funktionalitet, kan du ställa in `GenerateFanCylinder` egenskap av `Cylinder` klass till `true`. Följande kodsnutt visar hur denna funktionalitet ska användas:



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

![todo:image_alt_text](working-with-cylinder_3.png)

Den vänstra cylindern har `GenerateFanCylinder = false` och den högra har `GenerateFanCylinder = true`.
