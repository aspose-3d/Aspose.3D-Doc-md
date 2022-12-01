---
title: Save 3D cencene as HTML in C#
linktitle: Save 3D cencene as HTML
type: docs
weight: 90
url: /ar/net/save-3d-scene-as-html/
---
## **Oفيرفيو**

Tمقاله يوضح كيف يمكنك تحويل الملفات 3D إلى HTML بعد[تحميلها في كائن Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)باستخدام C# ويغطي مجموعة واسعة من المواضيع (النظر[تنسيقات الملفات المدعومة](https://docs.aspose.com/3d/net/supported-file-formats/)) على سبيل المثال

- Convert 3DS إلى HTML باستخدام C#
- Convert FBX إلى HTML في C#
- Convert STL إلى HTML في C#
- Convert U3D إلى HTML في C#
- Convert OBJ إلى HTML في C#


{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.9 أو أكبر.

{{% /alert %}} 
## **Save 3D cencene as HTML**
Aspose.3D for .NET يوفر `Html5SaveOptions` فئة لإنقاذ 3D المشهد كما HTML. Hen hen يمكنك تصدير المشهد إلى ملف HTML5 ، سوف API تصدير ثلاثة ملفات ، ملف `HTML` ، ملف Aspose3 eb eb eb (*.**A3dw**) ، وتقديم ملف 'JavaScript'. In الطلب على تصدير ملف a3dw فقط ، يمكنك تحديد Aspose3 eb eb eb كنوع التصدير ، وإعادة استخدام ملف criavaScript داخل صفحة HTML الخاصة بك. Tانه يتبع C# رمز قنص يظهر كيفية حفظ مشهد 3D كما HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

Due إلى الحدود الأمنية للمتصفح ، لا يمكن فتح ملف HTML المصدرة مباشرة ، تحتاج إلى فتحه من خلال خادم ويب ، إذا كان لديك python3 مثبت ، يمكنك بدء تشغيل خادم الويب في سطر الأوامر في الدليل المصدرة

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Tالدجاجة فتحه<http://localhost:8000/test.html>. The يستخدم بائع الويب ebebGL2 ، يمكنك استخدام<https://get.webgl.org/webgl2/>للتحقق مما إذا كان المتصفح يدعم ذلك أم لا.


