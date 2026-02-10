---
title: Working مع Linear Extrusion
type: docs
weight: 110
url: /ar/net/working-with-linear-extrusion/
description: Aspose.3D for .NET تقدم فئة triearextrusion ، والتي تأخذ شكل ثنائي الأبعاد كمدخل وتمتد الشكل في البعد الثالث.
---
#  **Pتشكيل Lineinextrusion**
Aspose.3D for .NET يقدم فئة `LinearExtrusion` ، والتي تأخذ شكل ثنائي الأبعاد كمدخل وتطيل الشكل في البعد الثالث. يظهر مقتطف الكود التالي كيفية إجراء البثق الخطي:



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
#  **'Liclic' في Linear xxtrusion**
Aspose.3D for .NET يوفر ملكية `Slices` من فئة `LinearExtrusion`. تحدد خاصية الشرائح عدد النقاط الوسيطة على طول مسار البثق. يظهر مقتطف الكود التالي كيفية استخدام خاصية الشرائح في البثق الخطي:



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
#  **'Enterالترفيه 'في Linear Extrusion**
Aspose.3D for .NET يوفر ملكية `Center` من فئة `LinearExtrusion`. إذا تم تعيين خاصية المركز إلى true ، يكون نطاق البثق من-الارتفاع/2 إلى الارتفاع/2 ، وإلا ، يكون البثق من 0 إلى الارتفاع. يظهر مقتطف الكود التالي كيفية استخدام خاصية المركز في البثق الخطي:



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
#  **'Tسوف' في Linear Extrusion**
Aspose.3D for .NET يوفر ملكية `Twist` من فئة `LinearExtrusion`. خاصية الالتواء تتعامل مع درجة الدوران أثناء بثق الشكل. يظهر مقتطف الكود التالي كيفية استخدام خاصية الالتواء في البثق الخطي:



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
#  **'TwistOffset' في Linear Extrusion**
Aspose.3D for .NET يوفر ملكية `TwistOffset` من فئة `LinearExtrusion`. خاصية الإزاحة الملتوية تترجم الإزاحة أثناء تدوير البثق. يظهر مقتطف الكود التالي كيفية استخدام خاصية الإزاحة الملتوية في البثق الخطي:



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
#  **'Direction' في Linear Extrusion**
Aspose.3D for .NET يوفر ملكية `Direction` من فئة `LinearExtrusion`. تحدد خاصية الاتجاه اتجاه البثق. يظهر مقتطف الكود التالي كيفية استخدام خاصية الاتجاه في البثق الخطي:



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
