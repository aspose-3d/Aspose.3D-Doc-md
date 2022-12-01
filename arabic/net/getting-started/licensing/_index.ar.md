---
title: Licensing
type: docs
weight: 60
url: /ar/net/licensing/
description: Overview من equiicensing equiequirements و valuation التقييم itations ersion تقليد لمعالجة 3D تنسيقات الملفات في C#.
---
Overview من equiicensing equiequirements و valuation التقييم itations ersion تقليد لمعالجة 3D تنسيقات الملفات في C#.

## **Eتقييم Vتقليد التقليد**
A نسخة تقييم مجانية من Aspose.3D for .NET يمكن تحميلها من قسم التنزيلات من موقع Aspose على العنوان التالي:[Ownتحميل Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
### **تقليد L**
Tانه نسخة التقييم يوفر جميع الميزات باستثناء ما يلي:

- يمكن sers sers فتح/استيراد الحد الأقصى من 50 3D الوثائق إلى cencene.
- Each عقدة يمكن أن يكون لا يزيد عن 5 عقدة الطفل.
- Each عقدة يمكن أن يكون لا يزيد عن 2 الكيانات المرفقة.
- Each الهندسة يمكن أن يكون لا يزيد عن 2 عناصر القشرة المرفقة.
- Each عقدة يمكن أن يكون لا يزيد عن 1 المواد.
- يمكن sers sers فقط حفظ الحد الأقصى من 50 3D الوثائق إلى cencene.
- سوف sers sers أيضا رؤية علامة مائية التقييم في الصور المقدمة وجميع ملفات الإخراج الأخرى.

{{% alert color="primary" %}} 
If كنت تستخدم Aspose.3D دون ترخيص مناسب ، يمكن أن يؤدي إلى `Aspose.ThreeD.TrialException` عندما بلغ الاستخدام القيود غير المرخصة ، يمكنك إيقاف تشغيل الاستثناء عن طريق:

* [Buy رخصة كاملة المواصفات] (https://purchase.asbos.com/buy).
* Request رخصة مؤقتة لمدة 30 يوما ، يرجى الرجوع إلى [How للحصول على Temporary Licance ؟] (https://purchase.aspos.com/temporary-license) Fأو المزيد من المعلومات.
.
* Set 'Aspose.ThreeD.TrialException. upuppressTrialException' إلى "الثقة" ، لن يتم رفع "xcrialException' خلال مكالمة" القلم O/ Save' على cencene ، ولكن لن يتم رفع القيود المذكورة أعلاه.
* استخدام عرضا كتلة 'محاولة/catch' على' cencene. Oالقلم/Save' ، وهذا الاستثناء هو مجرد إشعار ، تجاهل أنه لن يؤثر على تحميل المشهد/الادخار.

{{% /alert %}} 

## **Apply Lإيسنس باستخدام ile إيل أو Sترام Oحقن**
Tيمكن تحميل الترخيص من[ملف](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile)أو[كائن تيار](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET سوف نحاول العثور على الترخيص في المواقع التالية:

1. Explicit الطريق.
1. The المجلد الذي يحتوي على Aspose.3D.dll.
1. The المجلد الذي يحتوي على الجمعية التي تسمى Aspose.3D.dll.
1. Tانه مجلد يحتوي على تجميع الإدخال (الخاص بك. Exe).
1. An الموارد جزءا لا يتجزأ في الجمعية التي تسمى Aspose.3D.dll.

Tانه أسهل طريقة لتعيين الترخيص هو وضع ملف الترخيص في نفس المجلد مثل ملف Aspose.3D.dll وتحديد اسم الملف ، دون مسار ، كما هو موضح في المثال أدناه.

{{% alert color="primary" %}} 

إذا كنت تستخدم أي Aspose for .NET API أخرى جنبا إلى جنب مع Aspose.3D for .NET ، يرجى تحديد اسم الترخيص مثل `Aspose.ThreeD.License`.

{{% /alert %}} 
### **Lأودينغ icإيسنس من Fإيل**
Tانه أسهل طريقة لتطبيق الترخيص هو وضع ملف الترخيص في نفس المجلد مثل ملف Aspose.3D.dll وتحديد اسم الملف فقط دون مسار.

{{% alert color="primary" %}} 

When يمكنك الاتصال على طريقة `SetLicense` ، يجب أن يكون اسم الترخيص الذي تمر من ملف الترخيص. Fأو سبيل المثال ، إذا قمت بتغيير اسم ملف الترخيص إلى "Aspose.3D.lic. xml" تمرير اسم الملف إلى طريقة `threeD.SetLicense(…)`.

{{% /alert %}} 

**Example:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**Lأودينغ icإيسنس من Sترام Oبوكت**
Tانه يلي مثال يظهر كيفية تحميل ترخيص من تيار.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **Apply Lإيسنس باستخدام Embedded Resource**
One طريقة تطبيق ترخيص هو تعيينه[استخدام ملف أو كائن تيار](). Another طريقة أنيقة لتعبئة الترخيص مع التطبيق الخاص بك والتأكد من أنه لن يتم فقده هو تضمينه كمورد مضمن في واحدة من التجميعات التي تدعو component component component المكون (المدرجة في Aspose.3D).

Include o تضمين ملف الترخيص كمورد مضمن:

1. In Visual Studio .NET ، تشمل ملف الترخيص (. atic) في المشروع عن طريق اختيار**Fإيل**، ثم**Add xixisting tem tem**و أخيراً**Add**.
1. Elect تحديد الملف في Solution Explorer.
1. Set**Ction uild شفط**إلى**Embedded Resource**في نافذة roperties P.
1. To الوصول إلى الترخيص جزءا لا يتجزأ من التجمع (كمورد جزءا لا يتجزأ) ، مجرد إضافة ملف الترخيص كمورد جزءا لا يتجزأ من المشروع وتمرير اسم ملف الترخيص إلى طريقة SetLicance. Tانه Lفئة إيسنس تلقائيا يجد ملف الترخيص في الموارد جزءا لا يتجزأ. Tهنا ليست هناك حاجة إلى استدعاء أساليب semetExecutingAالجمعية و etetManifestResourceStream من Syالجذعية. eeflation. class فئة الجمعية في Microsoft .NET rramework.

Tانه يتبع رمز مقتطف يستخدم لتعيين الترخيص.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **Apply tered tered إيسنس**
Aspose.3D for .NET API يسمح للمطورين بتطبيق الترخيص المقنن. It هي آلية ترخيص جديدة. Tسيتم استخدام آلية الترخيص الجديدة جنبا إلى جنب مع طريقة الترخيص الحالية. يمكن للعملاء خرطوم Tالذين يرغبون في أن تكون فاتورة على أساس استخدام ميزات API استخدام الترخيص المقنن. Fأو المزيد من التفاصيل ، يرجى الرجوع إلى[Metered icensing FAQ](https://purchase.aspose.com/faqs/licensing/metered)القسم.

تم إضافة 07فئة جديدة [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) لتطبيق المفتاح المقنن. Tمثال التعليمات البرمجية له يوضح كيفية تعيين المفاتيح العامة والخاصة المقننة:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
