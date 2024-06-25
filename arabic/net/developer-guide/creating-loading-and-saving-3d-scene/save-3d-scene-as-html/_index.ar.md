---
title: وفِّر 3D مشهد بـ HTML في C#
linktitle: وفِّر 3D مشهد بـ HTML
type: docs
weight: 90
url: /ar/net/save-3d-scene-as-html/
---
##  **Oفيرفيو**

This article explains how you can convert 3D files to HTML after [loading them into Scene object](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) using C# and covers wide range of topics (considering [supported file formats](https://docs.aspose.com/3d/net/supported-file-formats/)) e.g.

- تحويل 3DS إلى HTML باستخدام C#
- تحويل FBX إلى HTML في C#
- تحويل STL إلى HTML في C#
- تحويل U3D إلى HTML في C#
- تحويل OBJ إلى HTML في C#


{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.9 أو أكبر.

{{% /alert %}} 
##  **وفِّر 3D مشهد بـ HTML**
Aspose.3D for .NET provides `Html5SaveOptions` class to save a save 3D scene as HTML. When you export the scene into HTML5 file, API will export three files, an `HTML` file, an Aspose3DWeb file(*.*a3dw**), and a rendered `JavaScript` file. In order to export a3dw file only, you can specify Aspose3DWeb as the export type, and reuse the JavaScript file within your own HTML page. The following C# code snippet shows how to save a 3D scene as HTML. 



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

نظرًا لحدود أمان المتصفح ، لا يمكن فتح ملف HTML الذي تم تصديره مباشرة ، تحتاج إلى فتحه من خلال خادم ويب ، إذا كان لديك تثبيت python3 ، يمكنك بدء تشغيل خادم الويب في سطر الأوامر في الدليل الذي تم تصديره

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Tالدجاجة فتحه<http://localhost:8000/test.html>. The يستخدم بائع الويب ebebGL2 ، يمكنك استخدام<https://get.webgl.org/webgl2/>للتحقق مما إذا كان المتصفح يدعم ذلك أم لا.


