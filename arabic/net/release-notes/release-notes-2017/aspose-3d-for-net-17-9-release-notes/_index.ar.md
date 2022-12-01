---
title: Aspose.3D for .NET 17.9 tes elease ootes
type: docs
weight: 40
url: /ar/net/aspose-3d-for-net-17-9-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.9](https://www.nuget.org/packages/Aspose.3D/17.9.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-286|دعم dd dd لتحديد شبكات فريدة من نوعها من FBX|ميزة ew ew|
|THREEDNET-288|دعم dd dd لتقديم المشهد في ظلال مخصصة بالكامل|ميزة ew ew|
|THREEDNET-284|Improof استهلاك الذاكرة عند كتابة ملف كبير FBX|Enhancement|
|THREEDNET-293|تصدير غير صحيحة OBJ مع نسيج إلى GLTF و GLB|Bug|
|THREEDNET-290|Rotation nimate خصائص دوران (Euler) scale لتنسيق FBX|Bug|
||||
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Member dds member reateAnimationCعضو الشفاه إلى Aspose.ThreeD.Scene الفئة**
It يساعد في خلق الرسوم المتحركة.

**Defintion C#**

{{< highlight "java" >}}

 /// <summary>

/// A shorthand function to create and register the <see cref="AnimationClip"/>

/// The first <see cref="AnimationClip"/> will be assigned to the <see cref="CurrentAnimationClip"/>

/// </summary>

/// <param name="name">Animation clip's name</param>

/// <returns></returns>

public Aspose.ThreeD.Animation.AnimationClip CreateAnimationClip(string name)

{{< /highlight >}}

Tله هو وظيفة قصيرة لإنشاء مقطع الرسوم المتحركة ، قبل إجراء هذه الوظيفة ، لإنشاء مقطع الرسوم المتحركة لديك ل:

**نهج egegence C#**

{{< highlight "java" >}}

 AnimationClip anim = new AnimationClip("anim");

scene.AnimationClips.Add(anim);

//set this as current clip

scene.CurrentAnimationClip = anim;

{{< /highlight >}}

Tانه ما يعادل رمز هو:

**Approach ew نهج C#**

{{< highlight "java" >}}

 //create an animation clip

AnimationClip anim = scene.CreateAnimationClip("anim");

{{< /highlight >}}

Tانه rereateAnimationCطريقة الشفاه سيجعل الشفاه nimnimationCفي مشهد.
#### **Member dds member reateAnimationNعضو ode إلى Aspose.ThreeD. nimnimation. nimnimationCفئة الشفاه**
It يساعد في خلق عقدة الرسوم المتحركة.

**Defintion C#**

{{< highlight "java" >}}

 /// <summary>

/// A shorthand function to create and register the animation node on current clip.

/// </summary>

/// <param name="nodeName">New animation node's name</param>

/// <returns></returns>

public Aspose.ThreeD.Animation.AnimationNode CreateAnimationNode(string nodeName)

{{< /highlight >}}

Tله هو وظيفة قصيرة لإنشاء وتسجيل onimationNode ، قبل هذه الوظيفة تحتاج إلى الكتابة:

**نهج egegence C#**

{{< highlight "java" >}}

 var anode = new AnimationNode("animRot");

anim.Animations.Add(anode);

{{< /highlight >}}

Tانه ما يعادل رمز هو:

**Approach ew نهج C#**

{{< highlight "java" >}}

 var anode = anim.CreateAnimationNode("animRot");

{{< /highlight >}}
#### **Adds ثلاثة أعضاء إلى Aspose.ThreeD. nimnimation. Cفئة urve**
All يساعد هؤلاء الأعضاء في إنشاء إطارات رئيسية.

**Defintion C#**

{{< highlight "java" >}}

 /// <summary>

/// Create a new key frame with specified value

/// A synonym of <see cref="CreateKeyFrame(double, float)"/>

/// </summary>

/// <param name="time">Time position(measured in seconds)</param>

/// <param name="value">The value at this time position</param>

public void Add(double time, float value)

/// <summary>

/// Create a new key frame with specified value

/// A synonym of <see cref="CreateKeyFrame(double, float, Interpolation)"/>

/// </summary>

/// <param name="time">Time position(measured in seconds)</param>

/// <param name="value">The value at this time position</param>

/// <param name="interpolation">The interpolation type of this key frame</param>

public void Add(double time, float value, Aspose.ThreeD.Animation.Interpolation interpolation)

/// <summary>

/// Gets the enumerator to traverse all key frames.

/// </summary>

/// <returns></returns>

public System.Collections.Generic.IEnumerator<Aspose.ThreeD.Animation.KeyFrame> GetEnumerator()

{{< /highlight >}}

The dd dd طرق هو مرادف ل rereateKeyFrame ، يتم وضع علامة على أساليب إعادة تدوير إعادة صياغة إعادة تسمية جميع الطرق كما obsoleted ، والطبقة ururve الآن ينفذ Inumerقابلة numer<KeyFrame>(حتى تتمكن من رؤية يتم إضافة العددي etetE) ، حتى تتمكن من الاستفادة من بناء جملة c # (Ref<https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/object-and-collection-initializers>) لتبسيط خلق منحنى.


#### **Member dds member indCعضو urve إلى Aspose.ThreeD. nimnimation. ururveMفئة الربط**


Tله سوف ربط البيانات منحنى على قناة موجودة في الربط urveMالربط.

**Defintion C#**

{{< highlight "java" >}}

 /// <summary>

/// Bind the curve to specified channel

/// </summary>

/// <param name="channelName">Which channel the curve will be bound to</param>

/// <param name="curve">The curve data</param>

public void BindCurve(string channelName, Aspose.ThreeD.Animation.Curve curve)

{{< /highlight >}}

Befront الإصدار 17.9 لإنشاء الرسوم المتحركة يدويا تحتاج إلى:

**C#**

{{< highlight "java" >}}

 //create a curve mapping on cube node's transform object, the curve manipulates the property 'Scale'

var scale = anode.CreateCurveMapping(cube1.Transform, "Scale");

// Create the animation curve on Y component of the scale 

Curve scaleYCurve = scale.CreateCurve("Y");

//let cube1.Transform.Scale.Y to be 1.0f at 0th sec using bezier interpolation

scaleYCurve.CreateKeyFrame(0, 1.0f, Interpolation.Bezier);

//let cube1.Transform.Scale.Y to be 2.0f at 2th sec using bezier interpolation

scaleYCurve.CreateKeyFrame(2, 2.0f, Interpolation.Bezier);

//let cube1.Transform.Scale.Y to be 0.2f at 5th sec using linear interpolation

scaleYCurve.CreateKeyFrame(5, 0.2f, Interpolation.Linear);

//let cube1.Transform.Scale.Y to be 1.0f at 8th sec using bezier interpolation

scaleYCurve.CreateKeyFrame(8, 1.0f, Interpolation.Bezier);

{{< /highlight >}}

Now في الإصدار 17.9 يمكنك تنفيذ نفس المهمة باستخدام السكر بناء الجملة:

**C#**

{{< highlight "java" >}}

 //create a curve mapping on cube node's transform object, the curve manipulates the property 'Scale'

var scale = anode.CreateCurveMapping(cube1.Transform, "Scale");

// Create the animation curve on Y component of the scale 

scale.BindCurve("Y", new Curve()

{

    //let cube1.Transform.Scale.Y to be 1.0f at 0th sec using bezier interpolation

    {0, 1.0f, Interpolation.Bezier},

    //let cube1.Transform.Scale.Y to be 2.0f at 2th sec using bezier interpolation

    {2, 2.0f, Interpolation.Bezier},

    //let cube1.Transform.Scale.Y to be 0.2f at 5th sec using linear interpolation

    {5, 0.2f, Interpolation.Linear},

    //let cube1.Transform.Scale.Y to be 1.0f at 8th sec using bezier interpolation

    {8, 1.0f, Interpolation.Bezier}

});

{{< /highlight >}}


#### **أعضاء dd dd hadhaderSet و reseresetShaders إلى Aspose.ThreeD.**
ShaderSet يسمح لك بتجاوز التنفيذ الافتراضي لـ Aspose.3D's renderer ، إذا قمت بتعيين مثال مخصص hadhaderSet ، فإن خاصية إعادة تعيين hadhadhadhad. uustomized ، إذا كنت ترغب في العودة إلى 07611348 مجموعة shader الافتراضية ، يمكنك تعيين hadresehaders. يمكننا السماح للمستخدم للسيطرة على آثار تجعل في حين أننا لا تزال توفر التنفيذ الخاصة بنا مع ما يكفي من التمدد.

**Defintion C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the shader set that used to render the scene

/// </summary>

Aspose.ThreeD.Render.ShaderSet ShaderSet{ get;set;}

/// <summary>

/// Gets or sets the preset shader set

/// </summary>

Aspose.ThreeD.Render.PresetShaders PresetShaders{ get;set;}

{{< /highlight >}}
#### **Adds Aspose.ThreeD. ender اندر. reseresehaders الفئة**
Ight ight الآن فقط متاح Default ، يمكن توفير أنماط أخرى مثل ظلال غير واقعية في المستقبل.

**Defintion C#**

{{< highlight "java" >}}

 /// <summary>

/// This defines the preset internal shaders used by the renderer.

/// </summary>

public enum PresetShaders

{

    /// <summary>

    /// Use the default shaders for phong/lambert/pbr materials

    /// </summary>

    Default,

    /// <summary>

    /// User's customized shader set

    /// </summary>

    Customized

}

{{< /highlight >}}


#### **Adds Aspose.ThreeD. ender اندر. hadhaderSet class**
It يساعد في تخصيص hadhaderProgram المستخدمة من قبل كل مواد مختلفة للسيطرة الكاملة على نتيجة العرض النهائية.

**Defintion C#**

{{< highlight "java" >}}

 /// <summary>

/// Shader programs for each kind of materials

/// </summary>

public class ShaderSet : IDisposable

{

    /// <summary>

    /// Gets or sets the shader that used to render the lambert material

    /// </summary>

    public ShaderProgram Lambert { get; set; }

    /// <summary>

    /// Gets or sets the shader that used to render the phong material

    /// </summary>

    public ShaderProgram Phong { get; set; }

    /// <summary>

    /// Gets or sets the shader that used to render the PBR material

    /// </summary>

    public ShaderProgram Pbr { get; set; }

    /// <summary>

    /// Gets or sets the fallback shader when required shader is unavailable

    /// </summary>

    public ShaderProgram Fallback { get; set; }

}

{{< /highlight >}}
#### **Renders المشهد في وضع Panorama مع ظلال مخصصة مع عمق linearized بدلا من الألوان.**
It يساعد في تخصيص hadhaderProgram المستخدمة من قبل كل مادة مختلفة للسيطرة الكاملة على نتيجة العرض النهائية.

**Defintion C#**

{{< highlight "java" >}}

 public void RenderPanoramaInDepth()

{

    string path = TestData + @"/textures/skybox2/skybox.obj";

    //load the scene

    Scene scene = new Scene(path);

    //create a camera for capturing the cube map

    Camera cam = new Camera(ProjectionType.Perspective);

    cam.NearPlane = 0.1;

    cam.FarPlane = 200;

    scene.RootNode.CreateChildNode(cam).Transform.Translation = new Vector3(5, 6, 0);

    cam.RotationMode = RotationMode.FixedDirection;

    //create two lights to illuminate the scene

    scene.RootNode.CreateChildNode(new Light() {LightType = LightType.Point}).Transform.Translation = new Vector3(-10, 7, -10);

    scene.RootNode.CreateChildNode(new Light()

    {

        LightType = LightType.Point,

        ConstantAttenuation = 0.1,

        Color = new Vector3(Color.CadetBlue)

        }).Transform.Translation = new Vector3(49, 0, 49);

        //create a render target

        using (var renderer = Renderer.CreateRenderer())

        {

            //Create a cube map render target with depth texture, depth is required when rendering a scene.

            IRenderTexture rt = renderer.RenderFactory.CreateCubeRenderTexture(new RenderParameters(false), 512, 512);

            //create a 2D texture render target with no depth texture used for image processing

            IRenderTexture final = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(false, 32, 0, 0), 1024 * 3 , 1024);

            //a viewport is required on the render target

            rt.CreateViewport(cam, RelativeRectangle.FromScale(0, 0, 1, 1));

            renderer.ShaderSet = CreateDepthShader(renderer);

            renderer.Render(rt);

            //execute the equirectangular projection post-processing with the previous rendered cube map as input

            PostProcessing equirectangular = renderer.GetPostProcessing("equirectangular");

            equirectangular.Input = rt.Targets[0];

            renderer.Execute(equirectangular, final);

            //save the texture into disk

            ((ITexture2D)final.Targets[0]).Save(RenderResult + "/depth-equirectangular.png", ImageFormat.Png);

        }

    }

private static ShaderSet CreateDepthShader(Renderer renderer)

{

    GLSLSource src = new GLSLSource();

    src.VertexShader = @"#version 330 core

    layout (location = 0) in vec3 position;

    uniform mat4 matWorldViewProj;

    out float depth;

    void main()

    {

        gl_Position = matWorldViewProj * vec4(position, 1.0f);

        float zfar = 200.0;

        float znear = 0.5;

        //visualize the depth by linearize it so we don't get a blank screen

        depth = (2.0 * znear) / (zfar + znear - gl_Position.z /gl_Position.w  * (zfar - znear));

    }";

    src.FragmentShader = @"#version 330 core

    in float depth;

    out vec4 color;

    void main()

    {

        color = vec4(depth, depth, depth, 1);

    }";

    //we only need the position to render the depth map

    VertexDeclaration fd = new VertexDeclaration();

    fd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);

    //compile shader from GLSL source code and specify the vertex input format

    var shader = renderer.RenderFactory.CreateShaderProgram(src, fd);

    //connect GLSL uniform to renderer's internal variable

    shader.Variables = new ShaderVariable[]

    {

        new ShaderVariable("matWorldViewProj", VariableSemantic.MatrixWorldViewProj)

    };

    //create a shader set

    ShaderSet ret = new ShaderSet();

    //we only use the fallback, and left other shaders unassigned, so all materials will be rendered by this shader

    ret.Fallback = shader;

    return ret;

}

{{< /highlight >}}

Uحكيم Examles

Pالإيجار تحقق من قائمة المواضيع المساعدة المضافة أو updated في مستندات Aspose.3D Wiki:

1. [Add nimnimation roroperty و eetop ararget Camera في 3D ile ile](/3d/ar/net/add-animation-property-and-setup-target-camera-in-3d-document/#addanimationpropertyandsetuptargetcamerain3ddocument-addanimationpropertyto3dscenedocument)
1. [Rأندر 3D cenسين مع Pأنوراما Mode في Depth](/3d/ar/net/render-3d-scene-with-panorama-mode-in-depth/)
