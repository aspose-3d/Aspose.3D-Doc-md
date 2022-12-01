---
title: Публичные API Изменения в Aspose.3D 1.7.0
type: docs
weight: 10
url: /ru/net/public-api-changes-in-aspose-3d-1-7-0/
---
**Содержание Резюме**

- [Добавляет Aspose.ThreeD.Entities.Frustum class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.Entities.Frustumclass)
- [Добавляет класс Aspose.ThreeD.ImageRenderOptions](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.ImageRenderOptionsclass)
- [Добавляет метод MoveForward в Aspose.ThreeD.Entities. Класс камеры](#PublicAPIChangesinAspose.3D1.7.0-AddsMoveForwardmethodinAspose.ThreeD.Entities.Cameraclass)
- [Добавляет членов CastShadows и ReceiveShadows в Aspose.ThreeD.Entities. Класс геометрии](#PublicAPIChangesinAspose.3D1.7.0-AddsCastShadowsandReceiveShadowsmembersinAspose.ThreeD.Entities.Geometryclass)
- [Добавляет метод GenerateNormal в класс Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D1.7.0-AddsGenerateNormalmethodinAspose.ThreeD.Entities.PolygonModifierclass)
- [Добавляет метод Concate в классе Aspose.ThreeD.Utilities.Quaternion](#PublicAPIChangesinAspose.3D1.7.0-AddsConcatemethodinAspose.ThreeD.Utilities.Quaternionclass)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 1.5.0 до 1.7.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
### **Добавляет Aspose.ThreeD.Entities.Frustum class**
Добавлен новый класс Frustum. Камера и свет были подклассами класса Entity. В версии 1.7.0 эти классы унаследованы от Frustum, а Frustum унаследован от Entity, поскольку свойства Position, Up, LookAt, Direction, Target, NearPlane и FarPlane извлекаются в Frustum.

**Извлеченные члены из Aspose.ThreeD.Entities.Camera в Aspose.ThreeD.Entities.Frustum** 
Все эти свойства извлекаются в Frustum:

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

**Вылеченные члены из класса Aspose.ThreeD.Entities.Light до Aspose.ThreeD.Entities.Frustum** 
Все эти свойства извлекаются в Frustum:

**C#**

{{< highlight "csharp" >}}

 Aspose.ThreeD.Node Target{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

{{< /highlight >}}
### **Добавляет класс Aspose.ThreeD.ImageRenderOptions**
**Конвертировать файл 3D в формат файла изображения**

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

**Добавлены участники в класс Aspose.ThreeD. Сцена:**

**C#**

{{< highlight "csharp" >}}

 public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format)

public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format, Aspose.ThreeD.ImageRenderOptions options)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap, Aspose.ThreeD.ImageRenderOptions options)

{{< /highlight >}}
### **Добавляет метод MoveForward в Aspose.ThreeD.Entities. Класс камеры**
Он перемещает камеру вперед к своей ориентации. Ориентация камеры определяется любой из Target/Direction/LookAt

- **Цель:**Целевой узел в пространстве, камера всегда будет смотреть на эту цель, независимо от того, что цель/камера изменила свое положение в пространстве.
- **LookAt:**Фиксированное положение в пространстве, камера всегда будет смотреть на это положение.
- **Направление:**Вектор направления, ориентация камеры напрямую определяется этим вектором, независимо от его положения.

Подпись метода:

**C#**

{{< highlight "csharp" >}}

 public void MoveForward(double distance)

{{< /highlight >}}
### **Добавляет членов CastShadows и ReceiveShadows в Aspose.ThreeD.Entities. Класс геометрии**
Некоторые форматы файлов могут хранить параметры, связанные с тенью, в геометрии, например FBX, и они также используются при рендеринге. В этом примере кода тени красного ящика и тора отбрасывают на плоскость, красная коробка не принимает тени, а синяя коробка не отбрасывает тени.

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
### **Добавляет метод GenerateNormal в класс Aspose.ThreeD.Entities.PolygonModifier**
Это позволяет разработчикам генерировать нормальные данные из экземпляра Mesh, если элемент VertexElementSmoothingGroup был определен на сетке, сгенерированные нормальные данные будут сглажены VertexElementSmoothingGroup.

Подпись метода:

**C#**

{{< highlight "csharp" >}}

 public static Aspose.ThreeD.Entities.VertexElementNormal GenerateNormal(Aspose.ThreeD.Entities.Mesh mesh)

{{< /highlight >}}

Код образца:

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
### **Добавляет метод Concate в классе Aspose.ThreeD.Utilities.Quaternion**
Это позволяет разработчикам конкатенировать два вращения в одно, представленное в Quaternion.

Подпись метода:

**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Utilities.Quaternion Concate(Aspose.ThreeD.Utilities.Quaternion rhs)

{{< /highlight >}}

Код образца:

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
