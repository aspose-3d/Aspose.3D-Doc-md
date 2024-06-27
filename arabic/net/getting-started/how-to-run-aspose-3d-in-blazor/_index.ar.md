---
title: كيف يتم تشغيل Aspose.3D في Blazor
type: docs
weight: 138
url: /ar/net/how-to-run-aspose-3d-in-blazor/
description: تعرف على كيفية تشغيل Aspose.3D في Blazor.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Oفيرفيو

Blazor هو إطار تطبيق ويب تم تطويره بواسطة Microsoft يسمح بكتابة تطبيقات الويب من جانب العميل باستخدام C# و .NET. تتميز بلازور باستخدامها لتقنية تجميع الويب ، والتي تمكن التطبيقات التي تعمل في المتصفح من استخدام رمز أصلي عالي الأداء. تستخدم بلازور بنية مكبرة ، مما يسمح للمطورين بتقسيم واجهة المستخدم إلى مكونات مستقلة ، وبالتالي تحقيق إعادة استخدام الكود وإمكانية الصيانة. تدعم Blazor التطوير عبر المنصات ويمكن تشغيلها على مجموعة متنوعة من المتصفحات والأجهزة الحديثة ، بما في ذلك أجهزة سطح المكتب والأجهزة المحمولة والأجهزة المدمجة.

بشكل عام ، توفر Blazor طريقة حديثة لبناء تطبيقات الويب ، مما يتيح للمطورين إنشاء تطبيقات ويب عالية الأداء وتفاعلية وقابلة للصيانة باستخدام تقنيات C# و .NET في المتصفح.

## أول تطبيق بليزر مع Aspose.3D

في هذا المثال ، أنشأنا تطبيق خادم Blazor بسيط ، وأنشأنا ملفًا ثلاثي الأبعاد ، وأخذنا لقطة شاشة لمحتوى الملف وعرضناه على صفحة ويب. أثناء عملية إنشاء المشروع ، يمكننا تكوينه وفقًا لاحتياجاتنا ، مثل التحقق من خيار "تمكين عامل الرصيف" بحيث يمكن بناء تطبيق Blazor وتشغيله في عامل الرصيف.

### قم بإنشاء أول تطبيق بليزور

دعنا نستخدم أداة VS2022 كمثال لإنشاء أول تطبيق بليزور بمبلغ Aspose.3D ، اتبع الخطوات أدناه:
1. حدد الملف-> جديد-> المشروع والتصفية باستخدام الكلمة الرئيسية بليزر لتحديد قالب المشروع المقابل.
<br>
<img src="1.png" width=80% />
1. تعيين اسم المشروع إلى "BlazorTest" وحدد المسار.
<br>
<img src="2.png" width=80% />
1. تكوين المكتبات والخيارات الأخرى المستخدمة في المشروع. أخيرًا ، انقر فوق الزر "إنشاء" لإنشاء مشروع السترة الأول.
<br>
<img src="3.png" width=80% />
1. بعد الدخول في المشروع ، انقر فوق "التبعيات" ضمن المشروع وحدد "إدارة الحزم NuGet"... لإضافة مكتبة Aspose.3D.
<br>
<img src="4.png" width=80% />
1. أدخل الكلمات الرئيسية لتصفية وتثبيت أحدث مكتبة Aspose.3D.
<br>
<img src="5.png" width=80% />
1. انقر نقرًا مزدوجًا على ملف "Index.razor" لتحرير المكتبة المطلوبة واستيرادها. إضافة بعض البيانات والصور.
<br>
<img src="5.png" width=80% />
1. تجميع المشروع وتشغيله ، وستحصل على النتائج التالية.
<br>
<img src="7.png" width=80% />

### عينة كود في تطبيق بليزور الأول

تم تضمين رمز العينة التالي في ملف Index.razor:
```
@page "/"
@using Aspose.ThreeD;
@using Aspose.ThreeD.Entities;
@using Aspose.ThreeD.Utilities;

<PageTitle>Index</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<SurveyPrompt Title="How is Blazor working for you?" />

<img src="@imageUrl" />

@code
{
    private string imageUrl="https://docs.aspose.com/3d/net/working-with-cylinder/working-with-cylinder_1.png";

    public Index()
    {
        CreateFile();
    }

    private void CreateFile()
    {
        // Create a scene
        Scene scene = new Scene();

        // Initialize cylinder
        var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

        // Set OffsetTop
        cylinder1.OffsetTop = new Vector3(5, 3, 0);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

        // Intialze second cylinder without customized OffsetTop
        var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder2);

        // Save
        scene.Save("CustomizedOffsetTopCylinder.obj");
    }
}

```