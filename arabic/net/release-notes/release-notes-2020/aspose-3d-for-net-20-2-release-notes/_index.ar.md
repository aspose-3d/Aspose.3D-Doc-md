---
title: Aspose.3D for .NET 20.2 tes elease ootes
type: docs
weight: 60
url: /ar/net/aspose-3d-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار معلومات عن Aspose.3D for .NET 20.2

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-612 |` `Igeneration generation متوافق الإجرائية I شكل الجيل|` `New ميزة|
|THREEDNET-615 |` `Igeneration generation متوافق الإجرائية C شكل الجيل|` `New ميزة|
|THREEDNET-616 |` `Igeneration generation متوافق الإجرائية Z شكل الجيل|` `New ميزة|
|THREEDNET-617 |` `Igeneration generation متوافق الإجرائية L شكل الجيل|` `New ميزة|
|THREEDNET-618 |` `Igeneration generation متوافق الإجرائية T شكل الجيل|` `New ميزة|
|THREEDNET-619 |` `Igeneration generation متوافق الإجرائية U شكل الجيل|` `New ميزة|
|THREEDNET-620 |` `Iprocedural generation متوافق الإجرائية مستطيل الشكل الجيل|` `New ميزة|
|THREEDNET-625 |` `Igeneration C متوافق مع شكل دائرة إجرائية الجيل|` `New ميزة|
|THREEDNET-626 |` `Igeneration C متوافق مع الشكل الناقص الإجرائي الجيل|` `New ميزة|
|THREEDNET-558 |` `Add دعم تقديم الشفافية في بائع الويب|` `Enhancement|
|THREEDNET-606 |` ` iisplay صندوق الحدود إذا تم اختيار العقدة في متصفح sset A.|` `Enhancement|
|THREEDNET-613 |` `Add دعم تقديم الشكل|` `Enhancement|
|THREEDNET-630 |` ` rorocess معلقة عند تحميل الملفات RVM|` `Bug|
|THREEDNET-632 |` `Exception على تحميل FBX ملف|` `Bug|
|THREEDNET-629 |` ` عدم الانزلاق على تحويل GLB إلى ثلاثية الأبعاد|` `Bug|
|THREEDNET-623 |لا يتم دعم ` `Intel's renU من قبل المورد Aspose.3D|` `Bug|
|THREEDNET-628 |` `Exception على تحميل FBX ملف|` `Bug|
## **Hangublic API و ackackward hangمتوافق مع hangمعلقة**
### **Added فئة جديدة Aspose.ThreeD. rروفيل.**
Tفئته هي الطبقة الأساسية لجميع التشكيلات الجانبية ، والتي يمكن استخدامها لإنشاء شبكات البارامترات. فئة A Profile يمثل ملف تعريف 2D في طائرة x-y.

{{< highlight "java" >}}

     /// <summary>

    /// 2D Profile in xy plane

    /// </summary>

    public abstract class Profile : Entity

    {

        /// <summary>

        /// Gets the extent in x and y dimension.

        /// </summary>

        /// <returns></returns>

        public abstract Vector2 GetExtent();

    }

    /// <summary>

    /// The base class of all parameterized profiles.

    /// </summary>

    public abstract class ParameterizedProfile : Profile

    {

    }

{{< /highlight >}}

All يمكن تحويل الفئة الفرعية من rofile Pإلى شبكة 3D من خلال شبكة inearExtrusion كما هو موضح في رمز العينة التالي:



{{< highlight "java" >}}

 var mesh = new LinearExtrusion(new LShape()

    {

     FilletRadius = 1,

     Width = 4,

     Depth = 7

      }, 1);

Scene s = new Scene(mesh);

s.Save(@"LShape.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
### **Added فئة جديدة Aspose.ThreeD. rروفيل. CircleShape**
يمكن توضيح roperties من irircleShape في الشكل أدناه.

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_1.png)
### **Added فئة جديدة Aspose.ThreeD. rروفيل. CShape**
يمكن توضيح roperties من Chhape في الشكل التالي:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_2.png)
### **Added فئة جديدة Aspose.ThreeD. rروفيل. EllipseShape**
يمكن توضيح roperties من EllipseShape في هذا الشكل:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_3.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل. HShape**
يمكن توضيح roperties من Hape hape في هذا الرقم:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_4.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل. LShape**
يمكن توضيح roperties من Lape hape في هذا الرقم:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_5.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل. ecectangleShape**
يمكن توضيح roperties من RectangleShape في هذا الرقم:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_6.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل.**
يمكن توضيح roperties من raprapeziumShape في هذا الشكل:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_7.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل. TShape**
يمكن توضيح roperties من Thhape في الشكل التالي:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_8.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل. UShape**
يمكن توضيح roperties من Uhhape في الشكل التالي:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_9.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل. ZShape**
يمكن توضيح roperties من Zhhape في الشكل التالي.

![تودو: الصورة_البديل_نص](aspose-3d-for-net-20-2-release-notes_10.png)


### **Added فئة جديدة Aspose.ThreeD. rروفيل.**
يحدد ملف التعريف الخاص به ملف تعريف جديد عن طريق تطابق الملف الشخصي الأساسي حول المحور y.

{{< highlight "java" >}}

 var mesh = new LinearExtrusion(new MirroredProfile(new LShape()

            {

                FilletRadius = 1,

                Width = 4,

                Depth = 7

            }), 1);

Scene s = new Scene(mesh);

s.Save(@"MirroredLShape.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

