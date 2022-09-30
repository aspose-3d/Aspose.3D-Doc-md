---
title: Save 3D cencene as HTML
type: docs
weight: 90
url: /ar/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.9 أو أكبر.

{{% /alert %}} 
# **Save 3D cencene as HTML**
Aspose.3D ل Python via .NET يوفر `Html5SaveOptions` فئة لحفظ 3D المشهد كما HTML. Hen hen يمكنك تصدير المشهد إلى ملف HTML5 ، سوف API تصدير ثلاثة ملفات ، ملف `HTML` ، ملف Aspose3 eb eb eb (*.**A3dw**) ، وتقديم ملف 'JavaScript'. In الطلب على تصدير ملف a3dw فقط ، يمكنك تحديد Aspose3 eb eb eb كنوع التصدير ، وإعادة استخدام ملف criavaScript داخل صفحة HTML الخاصة بك. Tانه يتبع رمز قنص يظهر كيفية حفظ مشهد 3D كما HTML.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

Due إلى الحدود الأمنية للمتصفح ، لا يمكن فتح ملف HTML المصدرة مباشرة ، تحتاج إلى فتحه من خلال خادم ويب ، إذا كان لديك python3 مثبت ، يمكنك بدء تشغيل خادم الويب في سطر الأوامر في الدليل المصدرة

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Tالدجاجة فتحه<http://localhost:8000/test.html>. The يستخدم بائع الويب ebebGL2 ، يمكنك استخدام<https://get.webgl.org/webgl2/>للتحقق مما إذا كان المتصفح يدعم ذلك أم لا.


