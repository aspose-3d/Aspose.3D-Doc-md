---
title: Public API Changements dans Aspose.3D 1.7.0
type: docs
weight: 10
url: /fr/net/public-api-changes-in-aspose-3d-1-7-0/
---
**Résumé du contenu**

- [Ajoute Aspose.ThreeD. Entités. Frustum class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.Entities.Frustumclass)
- [Ajoute Aspose.ThreeD. Classe ImageRenderOptions](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.ImageRenderOptionsclass)
- [Ajoute la méthode MoveForward en Aspose.ThreeD. Entités. Classe de caméra](#PublicAPIChangesinAspose.3D1.7.0-AddsMoveForwardmethodinAspose.ThreeD.Entities.Cameraclass)
- [Ajoute les membres CastShadows et ReceiveShadows au Aspose.ThreeD. Entités. Classe de géométrie](#PublicAPIChangesinAspose.3D1.7.0-AddsCastShadowsandReceiveShadowsmembersinAspose.ThreeD.Entities.Geometryclass)
- [Ajoute GenerateMéthode normale dans Aspose.ThreeD. Entités. Classe de polygonmodificateur](#PublicAPIChangesinAspose.3D1.7.0-AddsGenerateNormalmethodinAspose.ThreeD.Entities.PolygonModifierclass)
- [Ajoute la méthode Concate dans Aspose.ThreeD. Classe Utilities.Quaternion](#PublicAPIChangesinAspose.3D1.7.0-AddsConcatemethodinAspose.ThreeD.Utilities.Quaternionclass)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.3D API de la version 1.5.0 à 1.7.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses du Aspose.3D.

{{% /alert %}} 
### **Ajoute Aspose.ThreeD. Entités. Frustum class**
Une nouvelle classe Frustum est ajoutée. Caméra et Lumière étaient les sous-classes de la classe Entity. Dans la version 1.7.0, ces classes sont héritées de Frustum et Frustum est hérité d'Entity, car les propriétés Position, Up, LookAt, Direction, Target, NearPlane et FarPlane sont extraites dans Frustum.

**Membres extraits du Aspose.ThreeD. Entités. Caméra au Aspose.ThreeD. Entités. Frustum** 
Toutes ces propriétés sont extraites à Frustum:

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

**Membres extraits de la classe Aspose.ThreeD. Entités. Lumière à Aspose.ThreeD. Entités. Frustum** 
Toutes ces propriétés sont extraites à Frustum:

**C#**

{{< highlight "csharp" >}}

 Aspose.ThreeD.Node Target{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

{{< /highlight >}}
### **Ajoute Aspose.ThreeD. Classe ImageRenderOptions**
**Convertir un fichier 3D en format de fichier image**

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

**Membres ajoutés à la classe Aspose.ThreeD. Scène:**

**C#**

{{< highlight "csharp" >}}

 public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format)

public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format, Aspose.ThreeD.ImageRenderOptions options)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap, Aspose.ThreeD.ImageRenderOptions options)

{{< /highlight >}}
### **Ajoute la méthode MoveForward en Aspose.ThreeD. Entités. Classe de caméra**
Il avance la caméra vers son orientation. L'orientation d'une caméra est spécifiée par l'une des cibles/Direction/LookAt

- **Cible:**Un nœud cible dans l'espace, la caméra regardera toujours cette cible quel que soit la cible/la caméra a changé sa position dans l'espace.
- **LookAt:**Une position fixe dans l'espace, la caméra regardera toujours cette position.
- **Direction:**Un vecteur de direction, l'orientation d'une caméra est directement spécifiée par ce vecteur quelle que soit sa position.

Signature de la méthode:

**C#**

{{< highlight "csharp" >}}

 public void MoveForward(double distance)

{{< /highlight >}}
### **Ajoute les membres CastShadows et ReceiveShadows au Aspose.ThreeD. Entités. Classe de géométrie**
Certains formats de fichiers peuvent stocker des paramètres liés à l'ombre dans une géométrie comme FBX, et ils sont également utilisés dans le rendu. Dans cet exemple de code, les ombres de la boîte rouge et du tore projetées sur l'avion, la boîte rouge ne recevra pas d'ombres et la boîte bleue ne projettera pas d'ombres.

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
### **Ajoute GenerateMéthode normale dans Aspose.ThreeD. Entités. Classe de polygonmodificateur**
Il permet aux développeurs de générer des données normales à partir de l'instance Mesh, si l'élément VertexElementSmoothingGroup a été défini sur le maillage, les données normales générées seront lissées par le VertexElementSmoothingGroup.

Signature de la méthode:

**C#**

{{< highlight "csharp" >}}

 public static Aspose.ThreeD.Entities.VertexElementNormal GenerateNormal(Aspose.ThreeD.Entities.Mesh mesh)

{{< /highlight >}}

Code d'échantillon:

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
### **Ajoute la méthode Concate dans Aspose.ThreeD. Classe Utilities.Quaternion**
Il permet aux développeurs de concaténer deux transformations de rotation en une seule représentée en Quaternion.

Signature de la méthode:

**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Utilities.Quaternion Concate(Aspose.ThreeD.Utilities.Quaternion rhs)

{{< /highlight >}}

Code d'échantillon:

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
