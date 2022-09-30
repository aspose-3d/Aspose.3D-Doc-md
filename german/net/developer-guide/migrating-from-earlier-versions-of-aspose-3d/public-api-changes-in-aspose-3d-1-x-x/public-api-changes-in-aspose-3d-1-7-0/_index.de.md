---
title: Öffentliche API Änderungen in Aspose.3D 1.7.0
type: docs
weight: 10
url: /de/net/public-api-changes-in-aspose-3d-1-7-0/
---
**Inhalts übersicht**

- [Fügt Aspose.ThreeD. Entitäten. Frustum klasse hinzu](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.Entities.Frustumclass)
- [Fügt Aspose.ThreeD.Image Render Options klasse hinzu](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.ImageRenderOptionsclass)
- [Fügt die MoveForward-Methode in Aspose.ThreeD. Entitäten hinzu. Kamera klasse](#PublicAPIChangesinAspose.3D1.7.0-AddsMoveForwardmethodinAspose.ThreeD.Entities.Cameraclass)
- [Fügt Cast Shadows-und ReceiveShadows-Mitglieder in Aspose.ThreeD. Entitäten. Geometrie-Klasse hinzu](#PublicAPIChangesinAspose.3D1.7.0-AddsCastShadowsandReceiveShadowsmembersinAspose.ThreeD.Entities.Geometryclass)
- [Fügt Generate Normal-Methode in Aspose.ThreeD. Entitäten hinzu. Polygonmodifier-Klasse](#PublicAPIChangesinAspose.3D1.7.0-AddsGenerateNormalmethodinAspose.ThreeD.Entities.PolygonModifierclass)
- [Fügt die Concate-Methode in Aspose.ThreeD hinzu. Utilities.Quaternion-Klasse](#PublicAPIChangesinAspose.3D1.7.0-AddsConcatemethodinAspose.ThreeD.Utilities.Quaternionclass)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 1.5.0 bis 1.7.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **Fügt Aspose.ThreeD. Entitäten. Frustum klasse hinzu**
Eine neue Klasse Frustum wird hinzugefügt. Kamera und Licht waren die Unter klassen der Entität klasse. In der Version 1.7.0 werden diese Klassen von Frustum und Frustum von Entity geerbt, da die Eigenschaften Position, Up, LookAt, Direction, Target, NearPlane und Far Plane in Frustum extrahiert werden.

**Ausgezogene Mitglieder ab Aspose.ThreeD. Entitäten. Kamera an Aspose.ThreeD. Entitäten. Frustum** 
Alle diese Eigenschaften werden zu Frustum extrahiert:

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

**Ausgezogene Mitglieder aus der Klasse Aspose.ThreeD. Entitäten. Licht bis Aspose.ThreeD. Entitäten. Frustum** 
Alle diese Eigenschaften werden zu Frustum extrahiert:

**C#**

{{< highlight "csharp" >}}

 Aspose.ThreeD.Node Target{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

{{< /highlight >}}
### **Fügt Aspose.ThreeD.Image Render Options klasse hinzu**
**Konvertieren Sie eine Datei 3D in das Bilddatei format**

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

**Mitglieder zur Klasse Aspose.ThreeD hinzugefügt. Szene:**

**C#**

{{< highlight "csharp" >}}

 public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format)

public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format, Aspose.ThreeD.ImageRenderOptions options)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap, Aspose.ThreeD.ImageRenderOptions options)

{{< /highlight >}}
### **Fügt die MoveForward-Methode in Aspose.ThreeD. Entitäten hinzu. Kamera klasse**
Es bewegt sich vorwärts die Kamera in Richtung ihrer Ausrichtung. Die Ausrichtung einer Kamera wird durch ein Ziel/Richtung/LookAt angegeben

- **Ziel:**Als Ziel knoten im Raum betrachtet die Kamera dieses Ziel immer, unabhängig davon, was das Ziel/die Kamera seine Position im Raum geändert hat.
- **Blick auf:**Eine feste Position im Raum, die Kamera wird immer auf diese Position schauen.
- **Richtung:**Ein Richtungs vektor, die Ausrichtung einer Kamera, wird von diesem Vektor unabhängig von seiner Position direkt angegeben.

Methode Signatur:

**C#**

{{< highlight "csharp" >}}

 public void MoveForward(double distance)

{{< /highlight >}}
### **Fügt Cast Shadows-und ReceiveShadows-Mitglieder in Aspose.ThreeD. Entitäten. Geometrie-Klasse hinzu**
Einige Dateiformate können schatten bezogene Einstellungen in Geometrie wie FBXspeichern und werden auch beim Rendern verwendet. In diesem Code beispiel werden die Schatten der roten Box und des Torus in die Ebene geworfen, die rote Box erhält keine Schatten und die blaue Box wirft keine Schatten.

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
### **Fügt Generate Normal-Methode in Aspose.ThreeD. Entitäten hinzu. Polygonmodifier-Klasse**
Entwickler können normale Daten aus der Mesh-Instanz generieren. Wenn das VertexElementSmoothingGroup-Element im Netz definiert wurde, werden die generierten normalen Daten von der VertexElementSmoothingGroup geglättet.

Methode Signatur:

**C#**

{{< highlight "csharp" >}}

 public static Aspose.ThreeD.Entities.VertexElementNormal GenerateNormal(Aspose.ThreeD.Entities.Mesh mesh)

{{< /highlight >}}

Beispiel code:

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
### **Fügt die Concate-Methode in Aspose.ThreeD hinzu. Utilities.Quaternion-Klasse**
Es ermöglicht Entwicklern, zwei Rotations transformationen in eine in Quaternion dargestellte zu verkettieren.

Methode Signatur:

**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Utilities.Quaternion Concate(Aspose.ThreeD.Utilities.Quaternion rhs)

{{< /highlight >}}

Beispiel code:

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
