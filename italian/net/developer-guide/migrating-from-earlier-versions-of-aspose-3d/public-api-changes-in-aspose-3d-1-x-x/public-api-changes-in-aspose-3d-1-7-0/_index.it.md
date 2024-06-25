---
title: Variazioni pubbliche di API in Aspose.3D 1.7.0
type: docs
weight: 10
url: /it/net/public-api-changes-in-aspose-3d-1-7-0/
---
**Contenuto sommario**

- [Aggiunge Aspose. Classe ThreeD.Entities.Frustum](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.Entities.Frustumclass)
- [Aggiunge Aspose. Classe ThreeD.ImageRenderOptions](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.ImageRenderOptionsclass)
- [Aggiunge il metodo MoveForward in Aspose. Classe ThreeD.Entities.Camera](#PublicAPIChangesinAspose.3D1.7.0-AddsMoveForwardmethodinAspose.ThreeD.Entities.Cameraclass)
- [Aggiunge membri CastShadows e ReceiveShadows in Aspose.ThreeD.Entities.Geometry class](#PublicAPIChangesinAspose.3D1.7.0-AddsCastShadowsandReceiveShadowsmembersinAspose.ThreeD.Entities.Geometryclass)
- [Aggiunge il metodo GenerateNormal nella classe Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D1.7.0-AddsGenerateNormalmethodinAspose.ThreeD.Entities.PolygonModifierclass)
- [Aggiunge il metodo Concate in Aspose. Classe ThreeD.Utilities.Quaternion](#PublicAPIChangesinAspose.3D1.7.0-AddsConcatemethodinAspose.ThreeD.Utilities.Quaternionclass)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche a Aspose.3D API dalla versione da 1.5.0 a 1.7.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.3D.

{{% /alert %}} 
###  **Aggiunge Aspose. Classe ThreeD.Entities.Frustum**
Viene aggiunta una nuova classe Frustum. Camera e Luce erano le sottoclassi della classe Entity. Nella versione 1.7.0, queste classi vengono ereditate da Frustum e Frustum viene ereditato da Entity, poiché le proprietà Position, Up, LookAt, Direction, Target, NearPlane e FarPlane vengono estratte in Frustum.

**Membri estratti da Aspose.ThreeD.Entities.Camera a Aspose.ThreeD.Entities.Frustum** 
Tutte queste proprietà sono estratte a Frustum:

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

**Membri estratti dalla classe Aspose.ThreeD.Entities.Light to Aspose.ThreeD.Entities.Frustum** 
Tutte queste proprietà sono estratte a Frustum:

**C#**

{{< highlight "csharp" >}}

 Aspose.ThreeD.Node Target{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

{{< /highlight >}}
###  **Aggiunge Aspose. Classe ThreeD.ImageRenderOptions**
**Convertire un file 3D in formato file immagine**

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

**Aggiunti membri alla classe Aspose.ThreeD.Scene:**

**C#**

{{< highlight "csharp" >}}

 public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format)

public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format, Aspose.ThreeD.ImageRenderOptions options)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap, Aspose.ThreeD.ImageRenderOptions options)

{{< /highlight >}}
###  **Aggiunge il metodo MoveForward in Aspose. Classe ThreeD.Entities.Camera**
Si sposta in avanti la telecamera verso il suo orientamento. L'orientamento di una fotocamera è specificato da uno qualsiasi dei Target/Direction/LookAt

- **Obiettivo:**Un nodo target nello spazio, la fotocamera guarderà sempre questo obiettivo qualunque sia l'obiettivo/la telecamera che ha cambiato la sua posizione nello spazio.
- **LookAt:**Una posizione fissa nello spazio, la fotocamera guarderà sempre questa posizione.
- **Direzione:**Un vettore di direzione, l'orientamento di una telecamera è specificato direttamente da questo vettore qualunque sia la sua posizione.

Firma del metodo:

**C#**

{{< highlight "csharp" >}}

 public void MoveForward(double distance)

{{< /highlight >}}
###  **Aggiunge membri CastShadows e ReceiveShadows in Aspose.ThreeD.Entities.Geometry class**
Alcuni formati di file possono memorizzare le impostazioni relative alle ombre in geometria come FBX e vengono utilizzate anche nel rendering. In questo esempio di codice, le ombre della casella rossa e del toro proiettate sul piano, la casella rossa non riceverà ombre e la casella blu non proietterà ombre.

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
###  **Aggiunge il metodo GenerateNormal nella classe Aspose.ThreeD.Entities.PolygonModifier**
Consente agli sviluppatori di generare dati normali dall'istanza Mesh, se l'elemento VertexElementSmoothingGroup è stato definito sulla mesh, i dati normali generati verranno smussati da VertexElementSmoothingGroup.

Firma del metodo:

**C#**

{{< highlight "csharp" >}}

 public static Aspose.ThreeD.Entities.VertexElementNormal GenerateNormal(Aspose.ThreeD.Entities.Mesh mesh)

{{< /highlight >}}

Codice del campione:

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
###  **Aggiunge il metodo Concate in Aspose. Classe ThreeD.Utilities.Quaternion**
Consente agli sviluppatori di concatenare due trasformazioni di rotazione in una rappresentata in Quaternion.

Firma del metodo:

**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Utilities.Quaternion Concate(Aspose.ThreeD.Utilities.Quaternion rhs)

{{< /highlight >}}

Codice del campione:

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
