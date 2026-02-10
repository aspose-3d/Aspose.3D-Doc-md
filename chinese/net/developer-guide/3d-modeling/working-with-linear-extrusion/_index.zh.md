---
title: 与线性挤压一起工作
type: docs
weight: 110
url: /zh/net/working-with-linear-extrusion/
description: Aspose.3D for .NET 提供了linearexduting类，它采用2D形状作为输入，并在第三维中扩展该形状。
---
#  **进行线性挤压**
Aspose。3D for .NET 提供 `LinearExtrusion` 类，它将2D形状作为输入，并在第三维中扩展该形状。以下代码段显示了如何执行线性挤出:



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
#  **线性挤压中的 “切片”**
Aspose。3D for .NET 提供 `LinearExtrusion` 类的 `Slices` 属性。“切片” 属性定义沿挤出路径的中间点的数量。以下代码段显示了如何在线性挤出中使用 “切片” 属性:



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
#  **线性挤压中的 “中心”**
Aspose。3D for .NET 提供 `LinearExtrusion` 类的 `Center` 属性。如果 “中心” 特性设置为true，则挤出范围为从-Height/2到Height/2，否则，挤出范围为从0到Height。以下代码段显示了如何在线性挤出中使用中心属性:



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
#  **线性挤压中的 “扭曲”**
Aspose。3D for .NET 提供 `LinearExtrusion` 类的 `Twist` 属性。Twist属性处理挤出形状时的旋转程度。以下代码段显示了如何在线性挤出中使用Twist属性:



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
#  **线性挤压中的 “扭曲偏移”**
Aspose。3D for .NET 提供 `LinearExtrusion` 类的 `TwistOffset` 属性。旋转挤出时，“扭曲偏移” 属性会平移偏移。以下代码段显示了如何在线性挤出中使用TwistOffset属性:



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
#  **线性挤压中的 “方向”**
Aspose。3D for .NET 提供 `LinearExtrusion` 类的 `Direction` 属性。「方向」性质定义挤出的方向。以下代码段演示如何在线性挤出中使用Direction属性:



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
