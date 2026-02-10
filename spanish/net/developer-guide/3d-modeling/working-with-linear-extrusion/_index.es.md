---
title: Trabajando con extrusión lineal
type: docs
weight: 110
url: /es/net/working-with-linear-extrusion/
description: Aspose.3D for .NET ofrece la clase LinearExtrusion, que toma una forma 2D como entrada y extiende la forma en la tercera dimensión.
---
#  **Realización de extrusión lineal**
Aspose.3D for .NET ofrece la clase `LinearExtrusion`, que toma una forma 2D como entrada y extiende la forma en la 3ª dimensión. El siguiente fragmento de código muestra cómo realizar la extrusión lineal:



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
#  **'Slices' en extrusión lineal**
Aspose.3D for .NET ofrece la propiedad `Slices` de la clase `LinearExtrusion`. La propiedad Slices define el número de puntos intermedios a lo largo de la trayectoria de la extrusión. El siguiente fragmento de código muestra cómo utilizar la propiedad Slices en extrusión lineal:



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
#  **'Center' en extrusión lineal**
Aspose.3D for .NET ofrece la propiedad `Center` de la clase `LinearExtrusion`. Si la propiedad Center se establece en true, el rango de extrusión es de-Height/2 a Height/2; de lo contrario, la extrusión es de 0 a Height. El siguiente fragmento de código muestra cómo usar la propiedad Center en extrusión lineal:



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
#  **'Twist' en extrusión lineal**
Aspose.3D for .NET ofrece la propiedad `Twist` de la clase `LinearExtrusion`. La propiedad Twist controla el grado de rotación al extruir la forma. El siguiente fragmento de código muestra cómo utilizar la propiedad Twist en la extrusión lineal:



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
#  **'TwistOffset' en extrusión lineal**
Aspose.3D for .NET ofrece la propiedad `TwistOffset` de la clase `LinearExtrusion`. La propiedad Desfase de giro convierte el desfase mientras gira la extrusión. El siguiente fragmento de código muestra cómo usar la propiedad TwistOffset en la extrusión lineal:



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
#  **'Dirección' en extrusión lineal**
Aspose.3D for .NET ofrece la propiedad `Direction` de la clase `LinearExtrusion`. La propiedad Direction define la dirección de la extrusión. El siguiente fragmento de código muestra cómo utilizar la propiedad Direction en la extrusión lineal:



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
