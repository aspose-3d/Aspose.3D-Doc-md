---
title: Aspose.3D for .NET 22.2 tes elease ootes
type: docs
weight: 11
url: /ar/net/aspose-3d-for-net-22-2-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 22.2.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1054 |Embed llow تضمين القوام في U3D و PDF ملف|ميزة ew ew|
|THREEDNET-1058 |لا يمكن ربط ريمياثيس إلى المواد في USD المصدر/المستورد|إصلاح g ug|
|THREEDNET-1051 |إضافات الوصول Allow والإضافات في ملف GLTF|حركة بلا حدود|
|THREEDNET-1048 |Allow ترميز المشهد والبيانات الفوقية عقدة إلى usd|ميزة ew ew|
|THREEDNET-1049 |Allow فك المشهد والبيانات الفوقية عقدة من usd|ميزة ew ew|

## API التغييرات ##


### أعضاء Added إلى الفئة `Aspose.ThreeD.AssetInfo`:

{{< highlight "csharp" >}}
        public string Copyright{ get;set;}
{{< /highlight >}}

Gets حقوق الطبع والنشر للملف ، يمكن أن تكون هذه القيمة لاغية أو محددة في ملف 3D.
Only USC C/USDZ دعم هذه المنشأة الآن.

NOTE: hangمعلقة في هذه الخاصية لن تغير قسم حقوق الطبع والنشر من ملف الإخراج 3D.


### أعضاء Added إلى الفئة `Aspose.ThreeD.Formats.UsdSaveOptions`:

{{< highlight "csharp" >}}
        public bool ExportMetaData{ get;set;}
{{< /highlight >}}

Gets أو يحدد ما إذا كان تصدير معلومات الأصول المشهد وخصائص عقدة إلى الإخراج USDC/USDZ الملف.



### أعضاء Added إلى الفئة `Aspose.ThreeD.Formats.PdfSaveOptions`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Embed the external textures into the PDF file, default value is false.
        /// </summary>
        public bool EmbedTextures{ get;set;}
{{< /highlight >}}

Set هذا إلى true لتوليد ملف 3D PDF مع ملفات الملمس المضمنة.

Eرمز xample:

{{< highlight "csharp" >}}
        var scene = new Scene();
        scene.Open($"test.obj");
        var opt = new PdfSaveOptions();
        //embed the external textures in the output PDF file.
        opt.EmbedTextures = true;
        //Look up external textures in the  common/textures directory
        opt.LookupPaths.Add("common/textures");
        scene.Save("test.pdf", opt);
{{< /highlight >}}


### أعضاء Added إلى الفئة `Aspose.ThreeD.Formats.U3dSaveOptions`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Embed the external textures into the U3D file, default value is false.
        /// </summary>
        public bool EmbedTextures{ get;set;}
{{< /highlight >}}

Set هذا إلى true لتوليد ملف 3D U3D مع ملفات الملمس المضمنة.

Eرمز xample:

{{< highlight "csharp" >}}
        var scene = new Scene();
        scene.Open($"test.obj");
        var opt = new U3dSaveOptions();
        //embed the external textures in the output PDF file.
        opt.EmbedTextures = true;
        //Look up external textures in the  common/textures directory
        opt.LookupPaths.Add("common/textures");
        scene.Save("test.u3d", opt);
{{< /highlight >}}



