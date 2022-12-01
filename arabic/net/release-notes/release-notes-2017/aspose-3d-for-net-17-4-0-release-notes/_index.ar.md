---
title: Aspose.3D for .NET 17.4.0 tes elease oأوتس
type: docs
weight: 90
url: /ar/net/aspose-3d-for-net-17-4-0-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.4.0](https://www.nuget.org/packages/Aspose.3D/17.4.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-235|Add دعم تصدير نماذج 3D إلى Google Draco (.drc) تنسيق.|ميزة ew ew|
|THREEDNET-237|Improof حركة الكاميرا في وضع الإسقاط التقويمي.|Enhancement|
|THREEDNET-238|دعم dd dd zoom amamera|Enhancement|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Aving aving 3D Model في Google Draco (.drc) تنسيق**
Tلقد أضاف الإصدار الأخير من Aspose.3D for .NET API دعمًا لتصدير نماذج 3D إلى Google Draco (.drc). Dإيفليرز يمكن استيراد أي ملفات معتمدة 3D ، ومن ثم حفظ في شكل Google Draco.

Tمثال التعليمات البرمجية له يوضح كيفية تصدير نموذج 3D إلى تنسيق ملف Google Draco:

**.NET, C#**

{{< highlight "java" >}}

 //Create a new scene

var s = new Scene();

//Create a sphere object and attach it to the scene

s.RootNode.CreateChildNode("sphere", new Sphere());

//save it to file using draco format

s.Save("sphere.drc", FileFormat.Draco);

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.Draco.DracoCompressionLevel Enum**
يساعد racracoCompressionLevel Enum في تحديد مستوى ضغط قبل توفير نموذج 3D في تنسيق Google Draco (.drc).

Tانه يتبع رمز كامل من um نوم يدل على مستويات ضغط مختلفة مع الوصف:

**.NET, C#**

{{< highlight "java" >}}

 public enum DracoCompressionLevel

{

    /// <summary>

    /// No compression, this will result in the minimum encoding time.

    /// </summary>

    NoCompression,

    /// <summary>

    /// Encoder will perform a compression as quickly as possible.

    /// </summary>

    Fast,

    /// <summary>

    /// Standard mode, with good compression and speed.

    /// </summary>

    Standard,

    /// <summary>

    /// Encoder will compress the scene optimally, which may takes longer time to finish.

    /// </summary>

    Optimal

}

{{< /highlight >}}
### **Adds Aspose.ThreeD.**
تتيح فئة racracoSaveOptions للمطورين تطبيق الإعدادات قبل توفير نموذج 3D في تنسيق Google Draco (.drc).

Tانه يتبع رمز كامل من الطبقة يوضح جميع الخصائص مع الوصف:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Quantization bits for position

/// </summary>

public int PositionBits { get; set; }

/// <summary>

/// Quantization bits for texture coordinate

/// </summary>

public int TextureCoordinateBits { get; set; }

/// <summary>

/// Quantization bits for vertex color

/// </summary>

public int ColorBits { get; set; }

/// <summary>

/// Quantization bits for normal vectors

/// </summary>

public int NormalBits { get; set; }

/// <summary>

/// Compression level

/// </summary>

public DracoCompressionLevel CompressionLevel { get; set; }

{{< /highlight >}}
#### **Adds Aspose.ThreeD. orormat. racracoFormat lass**
Tله**Encode**طريقة من فئة racracoFormat يسمح للمطورين لترميز شبكة واحدة بدلا من المشهد كله ، وهو أكثر كفاءة.

Tانه يتبع رمز كامل من الطبقة يوضح طريقة Encode مع الوصف:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Encode the mesh to Draco mesh raw data

/// </summary>

/// <param name="mesh"></param>

/// <param name="options"></param>

/// <returns></returns>

public byte[]Encode(IMeshConvertible mesh, DracoSaveOptions options = null);

{{< /highlight >}}
#### **Encode esh sh في Google Draco (.drc) orormat**
The Draco ملف ليس لديه دعم المشهد الهرمي ، كل منهما. ملف جمهورية الكونغو الديمقراطية يمثل شبكة ، لذلك إنقاذ المشهد سوف دمج المشهد كله في شبكة واحدة ، والتي قد تفقد المعلومات.

Tمثال التعليمات البرمجية له يوضح كيفية ترميز ملاحظة في Google Draco (.drc) تنسيق:

**.NET, C#**

{{< highlight "java" >}}

 //Create a sphere

var mesh = new Sphere();

// Encode the sphere to Google Draco raw data using optimal compression level.

var b = FileFormat.Draco.Encode(mesh,

    new DracoSaveOptions() {CompressionLevel = DracoCompressionLevel.Optimal});

//Save the raw bytes to file

File.WriteAllBytes("sphere.drc", b);

{{< /highlight >}}
#### **Adds member otationMode عضو إلى Aspose.ThreeD. nntities. rurustum (Base فئة من amamera و ight ight)**
Tانه القيمة الافتراضية هي RotationMode. ixixedTarget ، يجعلها متوافقة مع التعليمات البرمجية القديمة في تقديم الوقت الحقيقي. If وضع دوران rurustum هو arixedTarget ، يتم تحديد اتجاه فروستوم من خلال خاصية ooookAt الخاصة بها التي هي موضع مطلق في مساحة العالم ، في هذا الوضع يمكن للمطورين دائما الحصول على خاصية استرداد مختلفة عند تغيير موقفها.

If وضع الدوران هو ixixedDirection ، سوف فروستوم لم تعد تنظر إلى الهدف ، ولكن الحفاظ على نفس الاتجاه (المحدد من قبل خاصية إعادة الاستصلاح D) بالنسبة إلى موقعها ، وهذا مفيد في تصميم أداة مثل CAD أو FPلعبة ، في هذا الوضع يمكن للمطورين دائما الحصول على مختلفة property ookAt الملكية عندما يحصل على تغيير وضعه.

Tمثال التعليمات البرمجية له يوضح كيفية تعيين وضع دوران amera C:

**.NET, C#**

{{< highlight "java" >}}

 Camera camera = new Camera();

camera.RotationMode = RotationMode.FixedDirection;

{{< /highlight >}}
#### **Adds member عضو التكاثر إلى Aspose.ThreeD. nntities. Cميرا lass**
Tهو القيمة الافتراضية (1 ، 1) ، تغيير هذه القيمة يمكن أن تجعل جداول الصور المقدمة في الاتجاه الأفقي/الرأسي في كاميرا تقويم العظام.

Tمثال التعليمات البرمجية له يوضح كيفية تعيين وضع دوران amera C:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the magnification used in orthographic camera

/// </summary>

public Vector2 Magnification { get;set; }

.................................................

Camera camera = new Camera();

camera.Magnification = new Vector2(2, 2);

{{< /highlight >}}
