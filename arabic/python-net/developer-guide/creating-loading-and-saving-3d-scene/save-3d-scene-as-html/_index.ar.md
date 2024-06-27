---
title: وفِّر 3D مشهد بـ HTML
type: docs
weight: 90
url: /ar/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.9 أو أكبر.

{{% /alert %}} 
#  **وفِّر 3D مشهد بـ HTML**
Aspose.3D for Python via .NET provides `Html5SaveOptions` class to save a save 3D scene as HTML. When you export the scene into HTML5 file, API will export three files, an `HTML` file, an Aspose3DWeb file(*.*a3dw**), and a rendered `JavaScript` file. In order to export a3dw file only, you can specify Aspose3DWeb as the export type, and reuse the JavaScript file within your own HTML page. The following code snippet shows how to save a 3D scene as HTML. 



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

نظرًا لحدود أمان المتصفح ، لا يمكن فتح ملف HTML الذي تم تصديره مباشرة ، تحتاج إلى فتحه من خلال خادم ويب ، إذا كان لديك تثبيت python3 ، يمكنك بدء تشغيل خادم الويب في سطر الأوامر في الدليل الذي تم تصديره

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Tالدجاجة فتحه<http://localhost:8000/test.html>. The يستخدم بائع الويب ebebGL2 ، يمكنك استخدام<https://get.webgl.org/webgl2/>للتحقق مما إذا كان المتصفح يدعم ذلك أم لا.


