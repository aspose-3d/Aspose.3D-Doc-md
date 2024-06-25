---
title: كيف يتم تشغيل Aspose.3D لـ. نت 6
type: docs
description: كيف يتم تشغيل Aspose.3D لـ. نت 6
weight: 138
url: /ar/net/how-to-run-aspose-3d-for-net6/
---
## Oفيرفيو

من أجل. منصات NET6 (أو الأحدث) ، مقارنة بالمنصات السابقة (.netcore31 أو قبل ذلك) ، هناك اختلاف مهم يتعلق بمكتبة الرسومات.
في هذا [مستند Microsoft](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only) الرسمي ، يشرح ذلك. NET6 أو الإصدارات الأحدث لمكتبة الرسومات "System.Drawing. المشترك" سيتم دعمه فقط على Windows ، ويقدم توصيات لاستبدال مكتبة الرسومات.

لمنتج Apose.3D ، لقد أجرينا التقييم وأكملنا ترحيل مكتبة الرسومات. نستخدم SkiaSharp بدلاً من System. Darking. شائع في الأنظمة غير Windows ، كما هو مقترح في الوثائق الرسمية لـ Microsoft. يرجى ملاحظة أن هذا التغيير الحرج سيدخل حيز التنفيذ في Aspose.3D 22.10.1 أو الأحدث. Net6.

لـ. netcore31 أو قبل ذلك ، من أجل التوافق والاستقرار ، ما زلنا نستخدم حاليًا مكتبة الرسومات "System.Drawing. المشترك". التبعيات لـ. netcore31 أو قبل ذلك هي كما يلي:
- النظام. الرسم. مشترك ، 4.7.0.
- النظام. الأمان. التشفير. Pkcs ، 5.0.1.
- System.Text.Encoding.CodePages ، 4.7.0.

## تشغيل Aspose.3D لـ. Net6 على Windows

أولاً ، يمكنك إنشاء تطبيق. net6 مع VS2022 ، ثم يمكنك اختيار خيارات التثبيت التالية:

### التثبيت من خلال nuget

1. Search for Aspose.3D from NuGet: [Aspose.3D for .NET NuGet Package](https://www.nuget.org/packages/Aspose.3D/). 
يمكنك أيضًا تثبيت Aspose.3D من مدير الحزم Nuget في VS2022.

2. سيتم تثبيت "SkiaSharp" أو "System.Drawing. المشترك" تلقائيًا كتبعية لـ Aspose.3D 22.10.1 أو الأحدث لـ. منصات Net6 ، والتي تعتمد على تكوين "نظام التشغيل المستهدف" في مشروعك.
- قم بتعيين "نظام التشغيل المستهدف" على "Windows" لمشروعك ، وسوف تستخدم "System.Drawing. المشترك" كاعتماد على نظام ويندوز الخاص بك. مشروع Net6. في هذا التكوين ، تكون نتيجة الرسم أقرب إلى. netcore31 أو قبل ذلك.
**! [التكوين الهدف os٨ (targetos.png)**
- تعيين "نظام التشغيل المستهدف" إلى "لا شيء" أو خيارات أخرى لمشروعك ، سوف تستخدم "SkiaSharp" كاعتماد على نظام ويندوز الخاص بك ل. مشروع Net6.*يرجى ملاحظة أن الإصدار الذي يستخدم "SkiaSharp" باعتباره تبعًا لا يدعم ميزة الطباعة على الطابعة.*

### تثبيت من خلال msi أو DLL

1. [تنزيل Aspose.3D.msi أو DLL](https://releases.aspose.com/3d/net/)

2. افتح دليل التثبيت أو دليل DLL ، ثم حدد الخطوة 3 أو 4 أدناه:

3. حدد موقع الدليل الفرعي net6.0-windows ، أضف Aspose.3D.dll إلى تطبيق. net6 الخاص بك. أضف يدويًا حزم nuget التالية إلى مشروع. net6 الخاص بك:
- النظام. الرسم. مشترك ، 4.7.0.
- النظام. الأمان. التشفير. Pkcs ، 6.0.3.
- System.Text.Encoding.CodePages ، 4.7.0.

بهذه الطريقة ، سوف تستخدم "System. Darwing. المشترك" كاعتماد على نظام ويندوز الخاص بك ل. مشروع Net6. في هذا التكوين ، تكون نتيجة الرسم أقرب إلى. netcore31 أو قبل ذلك.

4. حدد موقع الدليل الفرعي "net6.0" ، أضف Aspose.3D.dll فيه إلى تطبيق. net6 الخاص بك. أضف يدويًا حزم nuget التالية إلى مشروع. net6 الخاص بك:
- سكيشارب ، 2.88.6.
- النظام. الأمان. التشفير. Pkcs ، 6.0.3.
- System.Text.Encoding.CodePages ، 4.7.0.

بهذه الطريقة ، سوف تستخدم "SkiaSharp" كاعتماد على نظام ويندوز الخاص بك ل. مشروع Net6.*يرجى ملاحظة أن الإصدار الذي يستخدم "SkiaSharp" باعتباره تبعًا لا يدعم ميزة الطباعة على الطابعة.*
## تشغيل Aspose.3D لـ. Net6 على Linux

الرجوع إلى طريقة التثبيت على Windows ، يمكنك فقط تحديد SkiaSharp كتبعية لمكتبة الرسومات على نظام Linux.

تحتاج إلى القيام بالعمليات الإضافية التالية لضمان الاستخدام السليم لـ SkiaSharp تحت لينكس:

1. قم بتشغيل الأمر التالي في نظام Linux الخاص بك:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2. أضف حزم nuget "SkiaSharp.NativeAssets.Linux 2.88.6" إلى مشروعك. net6.

3. أو يمكنك اختيار إضافة حزم nuget "SkiaSharp.NativeAssets.Linux. Notendencies 2.88.6" إلى مشروعك. net6 ، بدلاً من الخطوتين أعلاه.

### مثال Dockerfile لأوبونتو

1. Add the nuget packages "SkiaSharp.NativeAssets.Linux 2.88.6" to your .net6 project.

2. استخدم Dockerfile التالي:
{{< highlight "plain" >}}
#  Ubuntu 20.04
FROM mcr.microsoft.com/dotnet/runtime:6.0-focal AS base
WORKDIR /app

#  add "libfontconfig1" package if using "SkiaSharp.NativeAssets.Linux" in your project
#  Or you need to use "SkiaSharp.NativeAssets.Linux.NoDependencies" in your project
RUN apt-get update && apt-get install -y libfontconfig1

#  Copy fonts from local to docker
#  For example, put a "fonts" folder in your project folder, and put the font files in it,
#  then, use the following line:
COPY fonts/ /usr/share/fonts

FROM mcr.microsoft.com/dotnet/sdk:6.0-focal AS build
WORKDIR /src
COPY ["Ubuntu_Docker.csproj", "."]
RUN dotnet restore "./Ubuntu_Docker.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "Ubuntu_Docker.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Ubuntu_Docker.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Ubuntu_Docker.dll"]
{{< /highlight >}}

### مثال Dockerfile لألبين

1. Add the nuget packages "SkiaSharp.NativeAssets.Linux 2.88.6" to your .net6 project.

2. استخدم Dockerfile التالي:
{{< highlight "plain" >}}
# Alpine 3.16
FROM mcr.microsoft.com/dotnet/runtime:6.0-alpine3.16 AS base
WORKDIR /app

#  add "fontconfig" package if using "SkiaSharp.NativeAssets.Linux" in your project
#  Or you need to use "SkiaSharp.NativeAssets.Linux.NoDependencies" in your project
RUN apk update && apk add fontconfig 

#  Copy fonts from local to docker
#  For example, put a "fonts" folder in your project folder, and put the font files in it,
#  then, use the following line:
COPY fonts/ /usr/share/fonts

FROM mcr.microsoft.com/dotnet/sdk:6.0-alpine3.16 AS build
WORKDIR /src
COPY ["Alpine_Docker.csproj", "."]
RUN dotnet restore "./Alpine_Docker.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "Alpine_Docker.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Alpine_Docker.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Alpine_Docker.dll"]
{{< /highlight >}}
