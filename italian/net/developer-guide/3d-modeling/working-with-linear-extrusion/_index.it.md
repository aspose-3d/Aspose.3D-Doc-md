---
title: Lavorare con l'estrusione lineare
type: docs
weight: 110
url: /it/net/working-with-linear-extrusion/
description: Aspose.3D for .NET offre la classe LinearExtrusion, che assume una forma 2D come input ed estende la forma nella terza dimensione.
---
#  **Eseguendo l'estrusione lineare**
Aspose.3D for .NET offre una classe `LinearExtrusion`, che assume una forma 2D come input ed estende la forma nella terza dimensione. Il seguente frammento di codice mostra come eseguire l'estrusione lineare:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize the base profile to be extruded
var profile = new RectangleShape()
{
    RoundingRadius = 0.3
};
// Perform Linear extrusion by passing a 2D profile as input and extend the shape in the 3rd dimension
var extrusion = new LinearExtrusion(profile, 10) { Slices = 100, Center = true, Twist = 360, TwistOffset = new Vector3(10, 0, 0) };
// Create a scene 
Scene scene = new Scene();
// Create a child node by passing extrusion 
scene.RootNode.CreateChildNode(extrusion);
// Save 3D scene
scene.Save("LinearExtrusion.obj");

{{< /highlight >}}
#  **'Affette' in estrusione lineare**
Aspose.3D for .NET offre `Slices` di proprietà della classe `LinearExtrusion`. La proprietà Slices definisce il numero di punti intermedi lungo il percorso dell'estrusione. Il seguente frammento di codice mostra come utilizzare la proprietà Slices nell'estrusione lineare:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize the base profile to be extruded
var profile = new RectangleShape()
{
    RoundingRadius = 0.3
};
// Create a scene 
Scene scene = new Scene();
// Create left node
var left = scene.RootNode.CreateChildNode();
// Create right node
var right = scene.RootNode.CreateChildNode();
left.Transform.Translation = new Vector3(15, 0, 0);
            
// Slices parameter defines the number of intermediate points along the path of the extrusion
// Perform linear extrusion on left node using slices property
left.CreateChildNode(new LinearExtrusion(profile, 2) { Slices = 2 });
// Perform linear extrusion on right node using slices property
right.CreateChildNode(new LinearExtrusion(profile, 2) { Slices = 10 });

// Save 3D scene
scene.Save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}
#  **"Centro" in estrusione lineare**
Aspose.3D for .NET offre `Center` di proprietà della classe `LinearExtrusion`. Se la proprietà Centro è impostata su true, l'intervallo di estrusione va da-Altezza/2 a Altezza/2, altrimenti l'estrusione è da 0 a Altezza. Il seguente frammento di codice mostra come utilizzare la proprietà Center nell'estrusione lineare:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize the base profile to be extruded
var profile = new RectangleShape()
{
    RoundingRadius = 0.3
};
// Create a scene 
Scene scene = new Scene();
// Create left node
var left = scene.RootNode.CreateChildNode();
// Create right node
var right = scene.RootNode.CreateChildNode();
left.Transform.Translation = new Vector3(15, 0, 0);
            
// Slices parameter defines the number of intermediate points along the path of the extrusion
// Perform linear extrusion on left node using slices property
left.CreateChildNode(new LinearExtrusion(profile, 2) { Slices = 2 });
// Perform linear extrusion on right node using slices property
right.CreateChildNode(new LinearExtrusion(profile, 2) { Slices = 10 });

// Save 3D scene
scene.Save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}
#  **'Twist' in Linear Extrusion**
Aspose.3D for .NET offre `Twist` di proprietà della classe `LinearExtrusion`. La proprietà Twist gestisce il grado di rotazione mentre si estrude la forma. Il seguente frammento di codice mostra come utilizzare la proprietà Twist nell'estrusione lineare:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize the base profile to be extruded
var profile = new RectangleShape()
{
    RoundingRadius = 0.3
};
// Create a scene 
Scene scene = new Scene();
// Create left node
var left = scene.RootNode.CreateChildNode();
// Create rifht node
var right = scene.RootNode.CreateChildNode();
left.Transform.Translation = new Vector3(15, 0, 0);

// Twist property defines the degree of the rotation while extruding the profile
// Perform linear extrusion on left node using twist and slices property
left.CreateChildNode(new LinearExtrusion(profile, 10) { Twist = 0, Slices = 100 });
// Perform linear extrusion on right node using twist and slices property
right.CreateChildNode(new LinearExtrusion(profile, 10) { Twist = 90, Slices = 100 });

// Save 3D scene
scene.Save("TwistInLinearExtrusion.obj");

{{< /highlight >}}
#  **"TwistOffset" nell'estrusione lineare**
Aspose.3D for .NET offre `TwistOffset` di proprietà della classe `LinearExtrusion`. La proprietà Twist Offset traduce l'offset durante la rotazione dell'estrusione. Il seguente frammento di codice mostra come utilizzare la proprietà TwistOffset nell'estrusione lineare:



{{< highlight "csharp" >}}
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Profiles;
using Aspose.ThreeD.Utilities;

// Initialize a Scene
Aspose.ThreeD.Scene scene = new Scene();

// Create a RectangleShape with width=2 and height=1
var rectangle = new RectangleShape()
{
    XDim = 2,
    YDim = 1
};

// Extrude the rectangle to create a 3D object (height=3)
var extrusion = new LinearExtrusion(rectangle, height: 3)
{
    Slices = 10 // Number of subdivisions along the extrusion path
};

// Add the extruded mesh to the scene
scene.RootNode.CreateChildNode(extrusion);

// Save the scene to a file
scene.Save("output.fbx", FileFormat.FBX7400ASCII);
{{< /highlight >}}
#  **«Direzione» in estrusione lineare**
Aspose.3D for .NET offre `Direction` di proprietà della classe `LinearExtrusion`. La proprietà di direzione definisce la direzione dell'estrusione. Il seguente frammento di codice mostra come utilizzare la proprietà Direction nell'estrusione lineare:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize the base profile to be extruded
var profile = new RectangleShape()
{
    RoundingRadius = 0.3
};
// Create a scene 
Scene scene = new Scene();
// Create left node
var left = scene.RootNode.CreateChildNode();
// Create right node
var right = scene.RootNode.CreateChildNode();
left.Transform.Translation = new Vector3(8, 0, 0);

// Direction property defines the direction of the extrusion.
// Perform linear extrusion on left node using twist and slices property
left.CreateChildNode(new LinearExtrusion(profile, 10) { Twist = 360, Slices = 100 });
// Perform linear extrusion on right node using twist, slices, and direction property
right.CreateChildNode(new LinearExtrusion(profile, 10) { Twist = 360, Slices = 100, Direction = new Vector3(0.3, 0.2, 1) });

// Save 3D scene
scene.Save("DirectionInLinearExtrusion.obj");

{{< /highlight >}}
