---
title: Offentlig API Ändrar i Aspose.3D 1.7.0
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-3d-1-7-0/
---
**Innehåll**

- [Adds Aspose.ThreeD.Entities.Frustum class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.Entities.Frustumclass)
- [Adds Aspose.ThreeD.ImageRenderOptions class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.ImageRenderOptionsclass)
- [Adds MoveForward method in Aspose.ThreeD.Entities.Camera class](#PublicAPIChangesinAspose.3D1.7.0-AddsMoveForwardmethodinAspose.ThreeD.Entities.Cameraclass)
- [Adds CastShadows and ReceiveShadows members in Aspose.ThreeD.Entities.Geometry class](#PublicAPIChangesinAspose.3D1.7.0-AddsCastShadowsandReceiveShadowsmembersinAspose.ThreeD.Entities.Geometryclass)
- [Adds GenerateNormal method in Aspose.ThreeD.Entities.PolygonModifier class](#PublicAPIChangesinAspose.3D1.7.0-AddsGenerateNormalmethodinAspose.ThreeD.Entities.PolygonModifierclass)
- [Adds Concate method in Aspose.ThreeD.Utilities.Quaternion class](#PublicAPIChangesinAspose.3D1.7.0-AddsConcatemethodinAspose.ThreeD.Utilities.Quaternionclass)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 1.5.0 till 1.7. 0, som kan vara av intresse för modul / applikationsutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Lägger till Aspose.ThreeD.Entiteter.Frustum klass**
En ny klass Frustum läggs till. Kamera och Ljus var underklasserna i enhetsklass. I version 1.7. Dessa klasser är ärvda från Frustum och Frustum ärvs från Entity, eftersom egenskaperna Position, Up, LookAt, Riktning, Target, NearPlane och FarPlane extraheras till Frustum.

**Extraherade medlemmar från Aspose ThreeD.Entites.Camera till Aspose.** 
Alla dessa egenskaper är extraherade till Frustum:

**C#**

{{< highlight "csharp" >}}

 Aspose.ThreeD.Utilities.Vector3 Position{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Up{ get;set;}

Aspose.ThreeD.Utilities.Vector3 LookAt{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

Aspose.ThreeD.Node Target{ get;set;}

double NearPlane{ get;set;}

double FarPlane{ get;set;}

{{< /highlight >}}

**Extraherade medlemmar från klassen Aspose ThreeD.Entites.Ljus till Aspose.** 
Alla dessa egenskaper är extraherade till Frustum:

**C#**

{{< highlight "csharp" >}}

 Aspose.ThreeD.Node Target{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

{{< /highlight >}}
###  **Lägger till Aspose.ThreeD.ImageRenderOptions Class.**
**Konvertera en 3D fil till bildfilformat.**

**C#**

{{< highlight "csharp" >}}

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

**Lagt till medlemmar i klassen Aspose.ThreeD.Scene:**

**C#**

{{< highlight "csharp" >}}

 public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format)

public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format, Aspose.ThreeD.ImageRenderOptions options)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap, Aspose.ThreeD.ImageRenderOptions options)

{{< /highlight >}}
###  **Lägger till MoveForward-metoden i Aspose.ThreeD.Entites.Camerklass**
Den går framåt kameran mot sin orientering. Kamerans orientering anges av något av Target/Direction/LookAt

- **Mål:**En målnod i rymden kommer kameran alltid att titta på detta mål oavsett mål/kameran har ändrat sin position i rymden.
- **Utsikt:**En fast position i rymden kommer kameran alltid att titta på denna position.
- **Riktning:**En riktningsvektor, en kamerans orientering anges direkt av denna vektor oavsett position.

Metodsignatur:

**C#**

{{< highlight "csharp" >}}

 public void MoveForward(double distance)

{{< /highlight >}}
###  **Lägger till CastShadows och mottagandeShadows medlemmar i Aspose.ThreeD.Entites.Geometry klass**
Vissa filformat kan lagra skuggrelaterade inställningar i geometri som FBX, och de används också i rendering. I detta kodexempel, skuggorna av den röda lådan och torus kastas till planet, Den röda lådan tar inte emot skuggor och blå lådan kastar inte skuggor.

**C#**

{{< highlight "csharp" >}}

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
###  **Lägger till GenereraNormal metod i Aspose. ThreeD.Entites.PolygonModifier Class.**
Det gör det möjligt för utvecklare att generera normala data från Mesh instans, om VertexElementSmoothingGroup element definierades på mesh, den genererade normala data kommer att jämnas ut av VertexElementSmoothingGroup.

Metodsignatur:

**C#**

{{< highlight "csharp" >}}

 public static Aspose.ThreeD.Entities.VertexElementNormal GenerateNormal(Aspose.ThreeD.Entities.Mesh mesh)

{{< /highlight >}}

Provkod:

**C#**

{{< highlight "csharp" >}}

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
###  **Lägger till Concate-metoden i Aspose.ThreeD.Utilities.Quaternion-klass**
Det tillåter utvecklare att sammanföra två rotationsomvandling till en representerad i Quaternion.

Metodsignatur:

**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Utilities.Quaternion Concate(Aspose.ThreeD.Utilities.Quaternion rhs)

{{< /highlight >}}

Provkod:

**C#**

{{< highlight "csharp" >}}

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
