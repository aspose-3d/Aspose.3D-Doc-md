---
title: Arbeiten mit linearer Extrusion
type: docs
weight: 110
url: /de/net/working-with-linear-extrusion/
description: Aspose.3D for .NET bietet LinearExtrusion-Klasse, die eine 2D-Form als Eingabe annimmt und die Form in der 3. Dimension erweitert.
---
#  **Lineare Extrusion durchführen**
Aspose.3D for .NET bietet `LinearExtrusion` Klasse, die eine 2D-Form als Eingabe annimmt und die Form in der 3. Dimension erweitert. Das folgende Code-Snippet zeigt, wie eine lineare Extrusion durchgeführt wird:



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
#  **"Slices" in der linearen Extrusion**
Aspose.3D for .NET bietet `Slices` Eigentum der `LinearExtrusion` Klasse. Die Slices-Eigenschaft definiert die Anzahl der Zwischen punkte entlang des Pfades der Extrusion. Das folgende Code-Snippet zeigt, wie die Slices-Eigenschaft bei der linearen Extrusion verwendet wird:



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
#  **"Zentrum" in der linearen Extrusion**
Aspose.3D for .NET bietet `Center` Eigentum der `LinearExtrusion` Klasse. Wenn die Center-Eigenschaft auf true gesetzt ist, reicht der Extrusion bereich von-Höhe/2 bis Höhe/2, andernfalls ist die Extrusion von 0 bis Höhe. Das folgende Code-Snippet zeigt, wie die Center-Eigenschaft in der linearen Extrusion verwendet wird:



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
#  **'Twist' in der linearen Extrusion**
Aspose.3D for .NET bietet `Twist` Eigentum der `LinearExtrusion` Klasse. Die Twist-Eigenschaft behandelt den Grad der Rotation, während die Form extrudiert wird. Das folgende Code-Snippet zeigt, wie die Twist-Eigenschaft bei der linearen Extrusion verwendet wird:



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
#  **'TwistOffset' in der linearen Extrusion**
Aspose.3D for .NET bietet `TwistOffset` Eigentum der `LinearExtrusion` Klasse. Twist Offset-Eigenschaft übersetzt den Versatz beim Drehen der Extrusion. Das folgende Code-Snippet zeigt, wie die TwistOffset-Eigenschaft in der linearen Extrusion verwendet wird:



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
#  **"Richtung" in der linearen Extrusion**
Aspose.3D for .NET bietet `Direction` Eigentum der `LinearExtrusion` Klasse. Die Richtungs eigenschaft definiert die Richtung der Extrusion. Das folgende Code-Snippet zeigt, wie die Direction-Eigenschaft bei der linearen Extrusion verwendet wird:



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
