---
title: Aspose.3D for .NET 18.7 - July 2018
type: docs
weight: 60
url: /ar/net/aspose-3d-for-net-18-7-july-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 18.7](https://www.nuget.org/packages/Aspose.3D/18.7.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-405|Add Draco 2.2 دعم الاستيراد|New eature|
|THREEDNET-406|Add Draco 2.2 دعم التصدير|New eature|
|THREEDNET-408|Import glTF الملفات مع ضغط دراكو|New eature|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **API التغييرات**
Tهنا نوعان من التغييرات الرئيسية:

1. تم إزالة بعض الطبقات والأساليب المتعرجة حسب الجدول الزمني ، يتم إزالة فئات XXclasses classes ononfig ، يجب على المستخدم استخدام ptions ptions ptions ptions ptions aveOptions و ptions ptions ptions ptions oadOالتي تم تقديمها في عام 2016.
1. File الاستيراد/التصدير ، هذه التغييرات لا تجعل أي تغييرات واجهة.
1. Google Draco تم تحديث دعم الاستيراد/التصدير إلى أحدث إصدار.
1. Aspose.3D 18.7 Cاستيراد glTF 2.0 الذي مكن ضغط دراكو.
#### **Rإموفيد الفئة Aspose.ThreeD. orأورماتس. Discreet3DSononfig**
#### **Rالرموز التعبيرية فئة Aspose.ThreeD. orormat. FBonononfig**
#### **Rالرموز التعبيرية فئة Aspose.ThreeD. orormat. bjbjConfig**
#### **Rالرموز التعبيرية فئة Aspose.ThreeD. orormat. STonononfig**
#### **Rالرموز التعبيرية فئة Aspose.ThreeD. orormat. Universal3DConfig**
#### **3 أعضاء إزالتها من الفئة Aspose.ThreeD. A3Db**
{{< highlight "java" >}}

         public Aspose.ThreeD.Property CreateDynamicProperty(string propName, System.Type type)

        public Aspose.ThreeD.Property CreateDynamicProperty(string propName)

        public Aspose.ThreeD.Property GetDynamicProperty(string propName)

{{< /highlight >}}

Use GetProperty/SetProperty بدلا من ذلك ، يتم إضافة GetProperty/SetProperty في 17.12.
#### **3 أعضاء إزالة من الفئة Aspose.ThreeD. nimnimation. ururve:**
{{< highlight "java" >}}

         public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time)

        public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time, float value)

        public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time, float value, Aspose.ThreeD.Animation.Interpolation interpolation)

{{< /highlight >}}

Use dd dd بدلا من ذلك ، يتم إضافة dd dd في 17.9 ، واستخدام dd dd بدلا من اسم آخر يمكن الاستفادة من C# تجميع بناء الجملة (<https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/object-and-collection-initializers>)
#### **3 أعضاء من الفئة Aspose.ThreeD. roroperty:**
{{< highlight "java" >}}

         public bool HasFlags(Aspose.ThreeD.PropertyFlags f)

        string ExtraData{ get;set;}

        Aspose.ThreeD.PropertyFlags Flags{ get;}

{{< /highlight >}}

يتم وضع علامة ese hese كما obsoleted منذ 18.2 ، وهذه هي أساسا للاستخدام الداخلي.
#### **4 طرق إزالتها من الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

         public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.IOConfig config)

        public void Open(string fileName, Aspose.ThreeD.Formats.IOConfig config)

        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.IOConfig config)

        public void Save(string fileName, Aspose.ThreeD.Formats.IOConfig config)

{{< /highlight >}}

Since لدينا XXptions ptions ptions aveOptions/Xptions ptions ptions ooadOptions لاستبدال ptions Xonononfig ، هذه الطرق تصبح عديمة الفائدة بعد إزالة Xoonononfig.
#### **3 طرق إزالتها من الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

         public double GetPitch()

        public double GetYaw()

        public double GetRoll()

{{< /highlight >}}

يتم وضع علامة ese hese كما obsoleted في 18.2 ، هناك طريقة استبدال EulerAngles().
#### **1 خاصية تضاف إلى الفئة Aspose.ThreeD. orormat. ptions bjLoadOptions:**
{{< highlight "java" >}}

         bool NormalizeNormal{ get;set;}

{{< /highlight >}}

Ets ets أو يحدد ما إذا كان لتطبيع ناقلات العادية أثناء التحميل ، القيمة الافتراضية صحيحة.
##### **Sرمز وافرة:**
{{< highlight "java" >}}

         Scene scene = new Scene();

        scene.Open("test.obj", new ObjLoadOptions() {NormalizeNormal = false});

{{< /highlight >}}

Tله سوف تحميل ملف obj وترك ناقلات العادية غير طبيعية ، فإن النسخة القديمة تطبيع ناقلات العادية عند تحميل ملف obj.
