---
title: إعداد مواد عادية أو فوق بالألوان فوق بالألوان المكعبة وإضافة مادة إلى كيانات 3D
type: docs
weight: 60
url: /ar/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java عروض لإدارة الأمور العادية وفوق البنفسجية على الأشكال الهندسية. تخزن الشبكة الخصائص الرئيسية لكل قمة ، وموضع في الفضاء ، ووضعه الطبيعي ، المعروف باسم متجه عمودي على السطح الأصلي. الطبيعي هو رئيسي في تعدادات التظليل ويجب أن يكون متجه وحدة. تدعم معظم تنسيقات الشبكات أيضًا بعض أشكال إحداثيات الموجات فوق الصوتية ، وهي تمثيل ثنائي الأبعاد منفصل للشبكة "غير مطوي" لإظهار أي جزء من خريطة نسيج ثنائي الأبعاد لتطبيقه على مضلعات مختلفة من الشبكة.
---
{{% alert color="primary" %}}

Aspose.3D for Java عروض لإدارة الأمور العادية وفوق البنفسجية على الأشكال الهندسية. تخزن الشبكة الخصائص الرئيسية لكل قمة ، وموضع في الفضاء ، ووضعه الطبيعي ، المعروف باسم متجه عمودي على السطح الأصلي. الطبيعي هو رئيسي في تعدادات التظليل ويجب أن يكون متجه وحدة. تدعم معظم تنسيقات الشبكات أيضًا بعض أشكال إحداثيات الموجات فوق الصوتية ، وهي تمثيل ثنائي الأبعاد منفصل للشبكة "غير مطوي" لإظهار أي جزء من خريطة نسيج ثنائي الأبعاد لتطبيقه على مضلعات مختلفة من الشبكة.

{{% /alert %}} {{% alert color="primary" %}}

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هنا](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) ثم نشير إلى عقدة الهندسة الشبكية من خلال إنشاء مشهد 3D.

{{% /alert %}}
##  **Create Nأورمال Vectors**
من أجل الحصول على نظرة بصرية جيدة على الإضاءة ، نحتاج إلى تحديد المعلومات العادية لكل قمة. من أجل الحصول على تفاصيل أفضل ، يمكننا أيضًا استخدام خريطة عادية ومنتشرة (استخدم خريطة ظل/منظر) لأداء كل بكسل عادي/لون. يتم تحقيق معلومات لكل قمة الرأس مثل اللون العادي أو الرأس بواسطة VertexElement. في Aspose.3D يمكننا رسم معلومات إضافية للتحكم في النقاط/الرأس المضلع/المضلع/الحافة ، عينة لتحديد الحالات العادية للقمة:

{{< highlight "java" >}}
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}


Tيتم تعيين 8 ناقلات طبيعية إلى نقاط التحكم 8 مباشرة ، في المثال التالي ، سنقوم بعرض سيناريو أكثر تعقيدا بعض الشيء.
##  **Ordinreate ordinordinordinالمرؤوسين**
Ere ere ، قمنا فقط بتحديد 4 إحداثيات V V ، ولكن تطبيقها على 24 vertices المضلع (6 face * 4 vertex لكل مضلع) باستخدام المؤشرات.
يوفر Aspose.3D 5 أوضاع تعيين:

- **Cأونت**-يتم تعيين كل البيانات إلى نقطة التحكم في الهندسة.
- **Pأوليغونط إرتكس**-يتم تعيين البيانات إلى قمة المضلع.
- **Pأوليغون**-يتم تعيين البيانات إلى المضلع.
- **Eدج**-يتم تعيين البيانات إلى الحافة.
- **AllSame**-بيانات واحدة مرسومة للهندسة بأكملها.



{{< highlight "java" >}}
// UVs
Vector4[] uvs = new Vector4[]
{
    new Vector4( 0.0, 1.0,0.0, 1.0),
    new Vector4( 1.0, 0.0,0.0, 1.0),
    new Vector4( 0.0, 0.0,0.0, 1.0),
    new Vector4( 1.0, 1.0,0.0, 1.0)
};
// Indices of the uvs per each polygon
int[] uvsId = new int[]
{
    0,1,3,2,2,3,5,4,4,5,7,6,6,7,9,8,1,10,11,3,12,0,2,13
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Create UVset
VertexElementUV elementUV = mesh.createElementUV(TextureMapping.DIFFUSE, MappingMode.POLYGON_VERTEX, ReferenceMode.INDEX_TO_DIRECT);
// Copy the data to the UV vertex element
elementUV.setData(uvs);
elementUV.setIndices(uvsId);
{{< /highlight >}}
##  **إضافة مواد إلى منتجات 3D**
Aspose.3D for Java يسمح للمطورين باستخدام خوارزمية التظليل لتظليل وإبراز دقيق. يحتوي الفونج على العديد من مدخلات الخرائط التي يمكننا استخدامها لإخفاء التأثير على العقدة. يأخذ التقديم القائم على أساس مادي (PBR) بعض الخصائص الفيزيائية للأشياء في الاعتبار ، ويوفر هذا النهج مظهر المواد كما هو الحال في العالم الحقيقي.
###  **Pهونغ Mالمواد مع إخراج Tل Cube**
Hen hen coordinates coordinates coordinates جاهزة للاستخدام ، يمكننا تطبيق نسيج على سطح الشبكة باستخدام المواد. Only فيرتكس اللون لا يمكن وصف تفاصيل السطح ، وهذا هو ما المواد المستخدمة ل. Here مثال على إرفاق مادة هونغ Pإلى عقدة مكعب:

{{< highlight "java" >}}
// Initialize scene object
Scene scene = new Scene();
// Initialize cube node object
Node cubeNode = new Node("cube");
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
// Point node to the mesh
cubeNode.setEntity(mesh);
// Add cube to the scene
scene.getRootNode().addChildNode(cubeNode);
// Initiallize PhongMaterial object
PhongMaterial mat = new PhongMaterial();
// Initiallize Texture object
Texture diffuse = new Texture();
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Set local file path
diffuse.setFileName(MyDir + "surface.dds");
// Set Texture of the material
mat.setTexture(Material.MAP_DIFFUSE, diffuse);
// Embed raw content data to FBX (only for FBX and optional)
// Set file name
diffuse.setFileName("embedded-texture.png");
// Set binary content
diffuse.setContent(Files.readAllBytes(Paths.get(MyDir, "aspose-logo.jpg")));
// Set color
mat.setSpecularColor(new Vector3(1, 0, 0));
// Set brightness
mat.setShininess(100);
// Set material property of the cube object
cubeNode.setMaterial(mat);
MyDir = MyDir + RunExamples.getOutputFilePath("MaterialToCube.fbx");
// Save 3D scene in the supported file formats
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}


We حدد رسم الخرائط نسيج منتشر ، ولون براق مع معلمة شينينس.
###  **Apply Phyبشكل هيسي ased R( PBR) Mإلى ox ox**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}
