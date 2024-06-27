---
title: كيف يتم تشغيل Aspose.3D في رصيف الميناء
type: docs
description: تشغيل Aspose.3D في حاوية إرساء لـ Linux وخادم Windows وأي نظام تشغيل.
weight: 139
url: /ar/net/how-to-run-aspose-3d-in-docker/
---
الخدمات الدقيقة ، جنبا إلى جنب مع حاويات تجعل من الممكن الجمع بين التقنيات بسهولة. يسمح لك عامل الميناء بدمج Aspose بسهولة. 3D في تطبيقك ، بغض النظر عن التكنولوجيا الموجودة في حزمة التطوير الخاصة بك.

في حال كنت تستهدف الخدمات المصغرة ، أو إذا كانت التقنية الرئيسية في المجموعة ليست .NET أو C++ أو Java ، ولكنك تحتاج إلى Aspose. وظيفة 3D ، أو إذا كنت تستخدم بالفعل عامل ميناء في المجموعة الخاصة بك ، فقد تكون مهتمًا باستخدام Aspose.3D في حاوية إرساء.

## المتطلبات

- يجب تثبيت عامل الميناء على النظام الخاص بك. للحصول على معلومات حول كيفية تثبيت عامل الميناء على Windows أو Mac ، راجع الارتباطات في قسم "انظر أيضًا".

- أيضًا ، لاحظ أن الاستوديو المرئي 2019 ، .NET Core 3.1 SDK يستخدم في المثال ، الوارد أدناه.


## تكميل

في هذا المثال ، ستقوم بإنشاء تطبيق وحدة تحكم بسيط يقوم بإنشاء ملف 3D وحفظه في جميع تنسيقات الحفظ المدعومة. يمكن بعد ذلك بناء التطبيق وتشغيله في عامل الميناء.

### إنشاء تطبيق وحدة التحكم

لإنشاء البرنامج ، اتبع الخطوات التالية:
1. بمجرد تثبيت عامل الميناء ، تأكد من أنه يستخدم حاويات لينكس (افتراضي). إذا لزم الأمر ، حدد خيار التبديل إلى حاويات Linux من قائمة أجهزة سطح مكتب Docker.
1. في الاستوديو المرئي ، أنشئ تطبيق وحدة التحكم الأساسية .NET.<br>
! [Todo: image_ altttext](create-a-new-project.png)<br>
1. تثبيت أحدث إصدار Aspose.3D من NuGet.<br>
! [Todo: image_ altttext](nuget-aspose-3d.png)<br>
1. بما أنه سيتم تشغيل التطبيق على لينكس ، يجب تثبيت أصول لينكس الأصلية المناسبة. ابدأ باستخدام صورة dotnet core sdk 3.1 وتثبيت libgdiblus base.
1. بعد إضافة جميع التبعيات المطلوبة ، اكتب برنامجًا بسيطًا ينشئ طائرة ويغير اتجاهها وحفظه لجميع تنسيقات الحفظ المدعومة:<br>
**.NET**<br>
{{< highlight "csharp" >}}
using System;
namespace Aspose.3D.Docker
{
    class Program
    {
        static void Main(string[] args)
        {
            // Initialize scene object
            Scene scene = new Scene();

            // Set Vector
            scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });

            //This will generate a plane that has customized orientation
            scene.Save("ChangePlaneOrientation.obj");
        }
    }
}

{{< /highlight >}}

لاحظ أن مجلد testoo out محدد كمجلد إخراج لحفظ مستندات الإخراج. عند تشغيل التطبيق في عامل الميناء ، سيتم تركيب مجلد على الجهاز المضيف على هذا المجلد في الحاوية. سيمكنك هذا من عرض المخرجات الناتجة عن Aspose بسهولة. 3D في حاوية رصيف الميناء.

### تكوين ملف Dockerfile

الخطوة التالية هي إنشاء ملف Dockerfile وتكوينه.

1. قم بإنشاء ملف Dockerfile ووضعه بجوار ملف حل طلبك. احتفظ باسم الملف هذا بدون امتداد (الافتراضي).
1. في Dockerfile ، حدد:

{{< highlight "plain" >}}
FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster 
COPY fonts/* /usr/share/fonts/
WORKDIR /app
COPY . ./
RUN apt-get update && \
    apt-get install -y --allow-unauthenticated libgdiplus libc6-dev
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

ما سبق هو ملف Dockerfile بسيط ، والذي يحتوي على الإرشادات التالية:

- صورة SDK التي سيتم استخدامها. هنا هو. صافي النواة SDK 3.1 صورة. سيقوم عامل ميناء بتنزيله عند تشغيل البناء. تم تحديد إصدار SDK كعلامة.
- الأمر لنسخ كل شيء إلى الحاوية ونشر التطبيق وتحديد نقطة الدخول.
- يتم تشغيل الأمر لتثبيت libgdiplus في الحاوية. هذا مطلوب بواسطة System.Drawing.Common.

### بناء وتشغيل التطبيق في ميناء

الآن يمكن بناء التطبيق وتشغيله في عامل الميناء. افتح موجه الأوامر المفضل لديك ، وقم بتغيير الدليل إلى المجلد باستخدام التطبيق (المجلد الذي يتم فيه وضع ملف الحل وملف Dockerfile) وتشغيل الأمر التالي:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

في المرة الأولى التي يتم فيها تنفيذ هذا الأمر ، قد يستغرق الأمر وقتًا أطول ، لأن عامل الميناء يحتاج إلى تنزيل الصور المطلوبة. بمجرد اكتمال الأمر السابق ، قم بتشغيل الأمر التالي:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

انتبه إلى حجة التثبيت ، لأنه ، كما ذكر سابقًا ، يتم تركيب مجلد على الجهاز المضيف في مجلد الحاوية ، لرؤية نتائج تنفيذ التطبيق بسهولة. المسارات في لينكس حساسة لحالة الأحرف.

{{% /alert %}}

## صور تدعم Aspose.3D

- Aspose. معيار 3D for .NET لا يدعم EMF و tif على Linux.


## مزيد من الأمثلة

***1. لتشغيل التطبيق بخادم Windows 2019***

- دوكيرفيل

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- بناء صورة عامل ميناء

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- تشغيل صورة عامل ميناء

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## انظر أيضًا

- [تثبيت سطح مكتب عامل ميناء على Windows](https://docs.docker.com/docker-for-windows/install/)
- [تثبيت سطح المكتب عامل ميناء على ماك](https://docs.docker.com/docker-for-mac/install/)
- [استوديو مرئي 2019 ، .NET Core 3.1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- خيار [التبديل إلى حاويات لينكس](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- معلومات إضافية عن [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
