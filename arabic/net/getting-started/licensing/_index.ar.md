---
title: Licensing
type: docs
weight: 60
url: /ar/net/licensing/
description: نظرة عامة على متطلبات Licensing وقيود إصدار التقييم لمعالجة تنسيقات ملفات 3D في C#.
---
نظرة عامة على متطلبات Licensing وقيود إصدار التقييم لمعالجة تنسيقات ملفات 3D في C#.

##  **Eتقييم Vتقليد التقليد**
إصدار تقييم مجاني من Aspose. يمكن تنزيل 3D for .NET من قسم التنزيلات في موقع Aspose على: [تنزيل Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
###  **تقليد L**
Tانه نسخة التقييم يوفر جميع الميزات باستثناء ما يلي:

- يمكن للمستخدمين فقط فتح/استيراد مستندات بقيمة 50 3D كحد أقصى للمشهد.
- Each عقدة يمكن أن يكون لا يزيد عن 5 عقدة الطفل.
- Each عقدة يمكن أن يكون لا يزيد عن 2 الكيانات المرفقة.
- Each الهندسة يمكن أن يكون لا يزيد عن 2 عناصر القشرة المرفقة.
- Each عقدة يمكن أن يكون لا يزيد عن 1 المواد.
- يمكن للمستخدمين فقط توفير 50 3D مستندات كحد أقصى في مشهد ما.
- سوف sers sers أيضا رؤية علامة مائية التقييم في الصور المقدمة وجميع ملفات الإخراج الأخرى.

{{% alert color="primary" %}} 
If you're using Aspose.3D without a proper license, there could trigger an `Aspose.ThreeD.TrialException` when the usage reached the unlicensed restrictions, you can turn the exception off by:

* [شراء ترخيص كامل المواصفات](https://purchase.aspose.com/buy).
* طلب ترخيص مؤقت لمدة 30 يومًا ، يرجى الرجوع إلى [كيف أحصل على ترخيص مؤقت ؟](https://purchase.aspose.com/temporary-license) لمزيد من المعلومات.
.
* Set `Aspose.ThreeD.TrialException.SuppressTrialException` to `true`, the `TrialException` will not be raised during the `Open/Save` call on Scene, but the above restrictions will not be lifted.
* استخدم يدويًا كتلة `try/catch` على `Scene.Open/Save` ، وهذا الاستثناء هو مجرد إشعار ، وتجاهله لن يؤثر على تحميل/توفير المشهد.

{{% /alert %}} 

##  **Apply Lإيسنس باستخدام ile إيل أو Sترام Oحقن**
يمكن تحميل الترخيص من [ملف](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) أو [كائن تيار](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose. سيحاول 3D for .NET العثور على الترخيص في المواقع التالية:

1. Explicit الطريق.
1. المجلد الذي يحتوي على Aspose.3D.dll.
1. المجلد الذي يحتوي على التجميع الذي يسمى Aspose.3D.dll.
1. Tانه مجلد يحتوي على تجميع الإدخال (الخاص بك. Exe).
1. مورد مضمّن في التجميع يسمى Aspose.3D.dll.

أسهل طريقة لتعيين ترخيص هي وضع ملف الترخيص في نفس المجلد مثل Aspose.3D.dll الملف وتحديد اسم الملف ، بدون مسار ، كما هو موضح في المثال أدناه.

{{% alert color="primary" %}} 

إذا كنت تستخدم أي Aspose for .NET API مع Aspose.3D for .NET ، يرجى تحديد مساحة الاسم للرخصة مثل `Aspose.ThreeD.License`.

{{% /alert %}} 
###  **Lأودينغ icإيسنس من Fإيل**
أسهل طريقة لتطبيق الترخيص هي وضع ملف الترخيص في نفس المجلد مثل Aspose.3D.dll الملف فقط وتحديد اسم الملف بدون مسار.

{{% alert color="primary" %}} 

عندما تتصل بطريقة `SetLicense` ، يجب أن يكون اسم الترخيص الذي تمرره هو اسم ملف الترخيص. على سبيل المثال ، إذا قمت بتغيير اسم ملف الترخيص إلى "Aspose.3D.lic.xml" مرر اسم الملف هذا إلى طريقة `threeD.SetLicense(…)`.

{{% /alert %}} 

**Example:**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
###  ` `**Lأودينغ icإيسنس من Sترام Oبوكت**
Tانه يلي مثال يظهر كيفية تحميل ترخيص من تيار.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
FileStream myStream = new FileStream("Aspose._3D.lic", FileMode.Open);
license.SetLicense(myStream);

{{< /highlight >}}
##  **Apply Lإيسنس باستخدام Embedded Resource**
إحدى الطرق لتطبيق الترخيص هي وضعه [استخدام ملف أو كائن تيار](). هناك طريقة أخرى أنيقة لتعبئة الترخيص مع تطبيقك والتأكد من أنه لن يتم فقده وهي تضمينه كمورد مضمن في إحدى التجميعات التي تستدعي DLL للمكون (مضمّن في Aspose.3D).

Include o تضمين ملف الترخيص كمورد مضمن:

1. في الاستوديو المرئي .NET ، قم بتضمين ملف ترخيص (.lic) في المشروع عن طريق الاختيار**Fإيل**، ثم**Add xixisting tem tem**و أخيراً**Add**.
1. Elect تحديد الملف في Solution Explorer.
1. Set**Ction uild شفط**إلى**Embedded Resource**في نافذة roperties P.
1. للوصول إلى الترخيص المضمّن في التجميع (كمورد مضمن) ، ما عليك سوى إضافة ملف الترخيص كمورد مضمن إلى المشروع وتمرير اسم ملف الترخيص إلى طريقة SetLicense. تعثر فئة الترخيص تلقائيًا على ملف الترخيص في الموارد المضمنة. ليست هناك حاجة لاستدعاء GetExecutingAssembly وطرق getement resourcestream للنظام. Refleck. Assembly في إطار Microsoft .NET.

Tانه يتبع رمز مقتطف يستخدم لتعيين الترخيص.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Instantiate the License class
Aspose.ThreeD.License license = new Aspose.ThreeD.License();

// Pass only the name of the license file embedded in the assembly
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
##  **Apply tered tered إيسنس**
Aspose.3D for .NET API يسمح للمطورين بتطبيق ترخيص مقاسات. إنها آلية ترخيص جديدة. سيتم استخدام آلية الترخيص الجديدة إلى جانب طريقة الترخيص الحالية. يمكن للعملاء الذين يرغبون في الحصول على فواتير بناءً على استخدام ميزات API استخدام الترخيص المقنن. لمزيد من التفاصيل ، يرجى الرجوع إلى قسم [مقننة Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered).

تمت إضافة فئة جديدة [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) لتطبيق المفتاح المقنن. يوضح هذا المثال البرمجي كيفية تعيين المفاتيح العامة والخاصة المقننة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a Metered license class object
Aspose.ThreeD.Metered metered = new Aspose.ThreeD.Metered();
// Set public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
