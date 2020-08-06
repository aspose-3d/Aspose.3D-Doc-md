---
title: Public API Changes in Aspose.3D 1.7.0
type: docs
weight: 10
url: /net/public-api-changes-in-aspose-3d-1-7-0/
---

**Contents Summary**

- [Adds Aspose.ThreeD.Entities.Frustum class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.Entities.Frustumclass)
- [Adds Aspose.ThreeD.ImageRenderOptions class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.ImageRenderOptionsclass)
- [Adds MoveForward method in Aspose.ThreeD.Entities.Camera class](#PublicAPIChangesinAspose.3D1.7.0-AddsMoveForwardmethodinAspose.ThreeD.Entities.Cameraclass)
- [Adds CastShadows and ReceiveShadows members in Aspose.ThreeD.Entities.Geometry class](#PublicAPIChangesinAspose.3D1.7.0-AddsCastShadowsandReceiveShadowsmembersinAspose.ThreeD.Entities.Geometryclass)
- [Adds GenerateNormal method in Aspose.ThreeD.Entities.PolygonModifier class](#PublicAPIChangesinAspose.3D1.7.0-AddsGenerateNormalmethodinAspose.ThreeD.Entities.PolygonModifierclass)
- [Adds Concate method in Aspose.ThreeD.Utilities.Quaternion class](#PublicAPIChangesinAspose.3D1.7.0-AddsConcatemethodinAspose.ThreeD.Utilities.Quaternionclass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.5.0 to 1.7.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **Adds Aspose.ThreeD.Entities.Frustum class**
A new class Frustum is added. Camera and Light were the subclasses of Entity class. In the version 1.7.0, these classes are inherited from Frustum and Frustum is inherited from Entity, since the properties Position, Up, LookAt, Direction, Target, NearPlane and FarPlane are extracted into Frustum.

**Extracted members from Aspose.ThreeD.Entities.Camera to Aspose.ThreeD.Entities.Frustum** 
All these properties are extracted to Frustum:

**C#**

{{< highlight csharp >}}

 Aspose.ThreeD.Utilities.Vector3 Position{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Up{ get;set;}

Aspose.ThreeD.Utilities.Vector3 LookAt{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

Aspose.ThreeD.Node Target{ get;set;}

double NearPlane{ get;set;}

double FarPlane{ get;set;}

{{< /highlight >}}

**Extracted members from class Aspose.ThreeD.Entities.Light to Aspose.ThreeD.Entities.Frustum** 
All these properties are extracted to Frustum:

**C#**

{{< highlight csharp >}}

 Aspose.ThreeD.Node Target{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

{{< /highlight >}}
### **Adds Aspose.ThreeD.ImageRenderOptions class**
**Convert a 3D file to image file format**

**C#**

{{< highlight csharp >}}

 // load an existing 3D scene

Scene scene = new Scene("test.obj");

// create a camera at (10,10,10) and look at the origin point for rendering, it must be attached to the scene before render

Camera camera = new Camera();

scene.RootNode.CreateChildNode("camera", camera);

camera.ParentNode.Transform.Translation = new Vector3(10, 10, 10);

camera.LookAt = Vector3.Origin;

//Specify the image render option

ImageRenderOptions opt = new ImageRenderOptions();

// set background color

opt.BackgroundColor = Color.AliceBlue;

// specify the path of textures

opt.AssetDirectories.Add(@"assets\textures");

// turn on shadow

opt.EnableShadows = true;

//render the scene in given camera's perspective into specified png file with size 1024x1024

scene.Render(camera, fileName, new Size(1024, 1024), ImageFormat.Png, opt);

{{< /highlight >}}

**Added members to class Aspose.ThreeD.Scene:**

**C#**

{{< highlight csharp >}}

 public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format)

public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format, Aspose.ThreeD.ImageRenderOptions options)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap, Aspose.ThreeD.ImageRenderOptions options)

{{< /highlight >}}
### **Adds MoveForward method in Aspose.ThreeD.Entities.Camera class**
It moves forward the camera towards its orientation. A camera's orientation is specified by any of the Target/Direction/LookAt

- **Target:** A target node in space, the camera will always look at this target whatever the target/camera has changed its position in space.
- **LookAt:** A fixed position in space, the camera will always look at this position.
- **Direction:** A direction vector, a camera's orientation is directly specified by this vector whatever its position is.

Method Signature:

**C#**

{{< highlight csharp >}}

 public void MoveForward(double distance)

{{< /highlight >}}
### **Adds CastShadows and ReceiveShadows members in Aspose.ThreeD.Entities.Geometry class**
Some file formats can store shadow related settings in geometry like FBX, and they're also used in rendering. In this code example, the shadows of the red box and torus cast to the plane, the red box won't receive shadows and blue box won't cast shadows.

**C#**

{{< highlight csharp >}}

 Scene scene = new Scene();

Camera camera = new Camera();

camera.NearPlane = 0.1;

scene.RootNode.CreateChildNode("camera", camera);

Light light;

scene.RootNode.CreateChildNode("light", light = new Light()

{

    NearPlane = 0.1,

    CastShadows =  true,

    Color = new Vector3(Color.White)

}).Transform.Translation = new Vector3(9.4785, 5, 3.18);

light.LookAt = Vector3.Origin;

light.Falloff = 90;

//Create a plane

Node plane = scene.RootNode.CreateChildNode("plane", new Plane(20, 20));

plane.Material = new PhongMaterial() {DiffuseColor = new Vector3(Color.DarkOrange)};

plane.Transform.Translation = new Vector3(0, 0, 0);

//Create a torus for casting shadows

Mesh m = (new Torus("", 1, 0.4, 20, 20, Math.PI*2)).ToMesh();

Node torus = scene.RootNode.CreateChildNode("torus", m);

torus.Material = new PhongMaterial() {DiffuseColor = new Vector3(Color.Cornsilk)};

torus.Transform.Translation = new Vector3(2, 1, 1);

{//Create a blue box don't cast shadows

    m = (new Box()).ToMesh();

    m.CastShadows = false;

    Node box = scene.RootNode.CreateChildNode("box", m);

    box.Material = new PhongMaterial() {DiffuseColor = new Vector3(Color.Blue)};

    box.Transform.Translation = new Vector3(2, 1, -1);

}

{// Create a red box that don't receive shadow but cast shadows

    m = (new Box()).ToMesh();

    m.ReceiveShadows = false;

    Node box = scene.RootNode.CreateChildNode("box", m);

    box.Material = new PhongMaterial() {DiffuseColor = new Vector3(Color.Red)};

    box.Transform.Translation = new Vector3(-2, 1, 1);

}

camera.ParentNode.Transform.Translation = new Vector3(10, 10, 10);

camera.LookAt = Vector3.Origin;

ImageRenderOptions opt = new ImageRenderOptions() {EnableShadows = true};

scene.Render(camera, "pic.png", new Size(1024, 1024), ImageFormat.Png, opt);

{{< /highlight >}}
### **Adds GenerateNormal method in Aspose.ThreeD.Entities.PolygonModifier class**
It allows developers to generate normal data from Mesh instance, if VertexElementSmoothingGroup element was defined on the mesh, the generated normal data will get smoothed by the VertexElementSmoothingGroup.

Method Signature:

**C#**

{{< highlight csharp >}}

 public static Aspose.ThreeD.Entities.VertexElementNormal GenerateNormal(Aspose.ThreeD.Entities.Mesh mesh)

{{< /highlight >}}

Sample Code:

**C#**

{{< highlight csharp >}}

 //Load a 3ds file, 3ds file doesn't have normal data, but it has smoothing group

Scene s = new Scene("test.3ds");

//Visit all nodes and create normal data for all meshes

s.RootNode.Accept(delegate(Node n)

{

    Mesh mesh = n.GetEntity<Mesh>();

    if (mesh != null)

    {

        VertexElementNormal normals = PolygonModifier.GenerateNormal(mesh);

        mesh.VertexElements.Add(normals);

    }

    return true;

});

{{< /highlight >}}
### **Adds Concate method in Aspose.ThreeD.Utilities.Quaternion class**
It allows developers to concatenate two rotation transformation into one represented in Quaternion.

Method Signature:

**C#**

{{< highlight csharp >}}

 public Aspose.ThreeD.Utilities.Quaternion Concate(Aspose.ThreeD.Utilities.Quaternion rhs)

{{< /highlight >}}

Sample Code:

**C#**

{{< highlight csharp >}}

 Scene scene = new Scene();

Quaternion q1 = Quaternion.FromEulerAngle(Math.PI * 0.5, 0, 0);

Quaternion q2 = Quaternion.FromAngleAxis(- Math.PI * 0.5, Vector3.XAxis);

//concatenate q1 and q2. q1 and q2 rotate alone x-axis with same angle but different direction, so the concatenated result will be identity quaternion.

Quaternion q3 = q1.Concate(q2);

//Create 3 cylinders to represent each quaternion

Node cylinder = scene.RootNode.CreateChildNode("cylinder-q1", new Cylinder(0.1, 1, 2));

cylinder.Transform.Rotation = q1;

cylinder.Transform.Translation = new Vector3(-5, 2, 0);

cylinder = scene.RootNode.CreateChildNode("cylinder-q2", new Cylinder(0.1, 1, 2));

cylinder.Transform.Rotation = q2;

cylinder.Transform.Translation = new Vector3(0, 2, 0);

cylinder = scene.RootNode.CreateChildNode("cylinder-q3", new Cylinder(0.1, 1, 2));

cylinder.Transform.Rotation = q3;

cylinder.Transform.Translation = new Vector3(5, 2, 0);

//Save to file

scene.Save("test.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
