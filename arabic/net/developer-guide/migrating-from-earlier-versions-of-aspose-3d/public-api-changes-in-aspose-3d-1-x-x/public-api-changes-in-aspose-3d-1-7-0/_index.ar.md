---
title: العام API يتغير بـ Aspose.3D 1.7.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-3d-1-7-0/
---
**Contents Sأوماري**

- [يضيف Aspose.ThreeD.Entities.Frustum class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.Entities.Frustumclass)
- [تضيف Aspose.ThreeD.ImageRenderOptions class](#PublicAPIChangesinAspose.3D1.7.0-AddsAspose.ThreeD.ImageRenderOptionsclass)
- [تضيف طريقة نقل إلى الأمام بـ Aspose.ThreeD. Enability. Camera class](#PublicAPIChangesinAspose.3D1.7.0-AddsMoveForwardmethodinAspose.ThreeD.Entities.Cameraclass)
- [يضيف CastShadows وأعضاء ReceiveShadows بـ Aspose.ThreeD.Entities.Geometry class](#PublicAPIChangesinAspose.3D1.7.0-AddsCastShadowsandReceiveShadowsmembersinAspose.ThreeD.Entities.Geometryclass)
- [يضيف طريقة GenerateNormal في Aspose.ThreeD. Enties. PolygonModifier class](#PublicAPIChangesinAspose.3D1.7.0-AddsGenerateNormalmethodinAspose.ThreeD.Entities.PolygonModifierclass)
- [تضيف طريقة كونكيت في Aspose.ThreeD. Utility. Quaternion class](#PublicAPIChangesinAspose.3D1.7.0-AddsConcatemethodinAspose.ThreeD.Utilities.Quaternionclass)

{{% alert color="primary" %}} 

يوضح هذا المستند التغييرات إلى Aspose.3D API من الإصدار 1.5.0 إلى 1.7.0 ، والتي قد تهم مطوري الوحدة/التطبيق. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **يضيف Aspose.ThreeD.Entities.Frustum class**
يتم إضافة A فئة جديدة rurustum. كانت amamera و ight ight الطبقات الفرعية من فئة Entity. In الإصدار 1.7.0 ، يتم inherهذه الطبقات من rurustum و rurustum من Entity ، حيث يتم استخراج خصائص sition osition ، Up ، ooookAt ، Direction ، ararget ، lane earPlane و FarPlane في rurustum.

**الأعضاء المستخرجون من Aspose.ThreeD. Entials. Camera إلى Aspose.ThreeD. Entials. Frustum** 
All يتم استخراج هذه الخصائص إلى الصدأ F:

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

**الأعضاء المستخرجون من الفئة Aspose.ThreeD. Enabilies. Light إلى Aspose.ThreeD.Entities.Frustum** 
All يتم استخراج هذه الخصائص إلى الصدأ F:

**C#**

{{< highlight "csharp" >}}

 Aspose.ThreeD.Node Target{ get;set;}

Aspose.ThreeD.Utilities.Vector3 Direction{ get;set;}

{{< /highlight >}}
###  **تضيف Aspose.ThreeD.ImageRenderOptions class**
**تحويل ملف 3D إلى تنسيق ملف صورة**

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

**أضاف أعضاء إلى الفصل Aspose.ThreeD.Scene:**

**C#**

{{< highlight "csharp" >}}

 public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format)

public void Render(Aspose.ThreeD.Entities.Camera camera, string fileName, System.Drawing.Size size, System.Drawing.Imaging.ImageFormat format, Aspose.ThreeD.ImageRenderOptions options)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap)

public void Render(Aspose.ThreeD.Entities.Camera camera, System.Drawing.Bitmap bitmap, Aspose.ThreeD.ImageRenderOptions options)

{{< /highlight >}}
###  **تضيف طريقة نقل إلى الأمام بـ Aspose.ThreeD. Enability. Camera class**
It يتحرك إلى الأمام الكاميرا نحو اتجاهها. يتم تحديد اتجاه الكاميرا A من قبل أي من ararget/Direction/ooookAt

- **Target:**A الهدف عقدة في الفضاء ، فإن الكاميرا ننظر دائما إلى هذا الهدف مهما كان الهدف/الكاميرا قد غيرت موقعها في الفضاء.
- **LookAt:**A موقف ثابت في الفضاء ، فإن الكاميرا ننظر دائما في هذا الموقف.
- **Direction:**A اتجاه ناقلات ، يتم تحديد اتجاه الكاميرا مباشرة من قبل هذا ناقلات مهما كان موقفها.

Method Signature:

**C#**

{{< highlight "csharp" >}}

 public void MoveForward(double distance)

{{< /highlight >}}
###  **يضيف CastShadows وأعضاء ReceiveShadows بـ Aspose.ThreeD.Entities.Geometry class**
يمكن لبعض تنسيقات الملفات تخزين الإعدادات المتعلقة بالظل في الهندسة مثل FBX ، ويتم استخدامها أيضًا في العرض. في هذا المثال الرمزي ، ظلال الصندوق الأحمر والحنجرة الملقاة على الطائرة ، لن يتلقى الصندوق الأحمر الظلال ولن يلقي الصندوق الأزرق ظلالاً.

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
###  **يضيف طريقة GenerateNormal في Aspose.ThreeD. Enties. PolygonModifier class**
It يسمح للمطورين لتوليد البيانات العادية من Mesh على سبيل المثال ، إذا تم تعريف عنصر mooertexEleالقابل moomoothingGroup على الشبكة ، فإن البيانات العادية التي تم إنشاؤها سوف تحصل على تمهيد من قبل erertexEleالقابل moomoothingGroup.

Method Signature:

**C#**

{{< highlight "csharp" >}}

 public static Aspose.ThreeD.Entities.VertexElementNormal GenerateNormal(Aspose.ThreeD.Entities.Mesh mesh)

{{< /highlight >}}

Sوافرة oode:

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
###  **تضيف طريقة كونكيت في Aspose.ThreeD. Utility. Quaternion class**
It يسمح للمطورين لربط اثنين من التحول دوران إلى واحد ممثلة في Quaternion.

Method Signature:

**C#**

{{< highlight "csharp" >}}

 public Aspose.ThreeD.Utilities.Quaternion Concate(Aspose.ThreeD.Utilities.Quaternion rhs)

{{< /highlight >}}

Sوافرة oode:

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
