---
title: Aspose.3D for .NET 18.9-سبتمبر 2018
type: docs
weight: 40
url: /ar/net/aspose-3d-for-net-18-9-september-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 18.9](https://www.nuget.org/packages/Aspose.3D/18.9.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-414|CanellationTدعم أوكين|New eature|
|THREEDNET-423|FBX ExportException-Hhigh olyأوليغون Count|Bug|
|THREEDNET-419|ImportException أثناء فتح ملفات ضخمة FBX|Bug|
|THREEDNET-421|يتم تحميل جميع الخصائص من FBX الإعدادات العالمية في AssetInfo|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
### **API التغييرات**
#### **Rالرموز التعبيرية فئة Aspose.ThreeD. tiliتيليتيز. upuple**
{{< highlight "java" >}}

 In order to use some advanced features(CancellationToken), we have dropped the support of .net 3.5, so some replacement classes are also removed.

{{< /highlight >}}
#### **Added مكان إقامة AssetInfo إلى الفئة Aspose.ThreeD.**
يمكن أن تتضمن أنواع ملفات ome معلومات الأصول لكل عقدة.
In FBX ، خاصية AssetInfo من عقدة الجذر تحتوي على الإعدادات العالمية المحددة في الملفات FBX.

{{< highlight "java" >}}

         /// <summary>

        /// Per-node asset info

        /// </summary>

        Aspose.ThreeD.AssetInfo AssetInfo{ get;set;}

{{< /highlight >}}

**Sوافرة oode:**

{{< highlight "java" >}}

         //Access GlobalSettings in FBX file, more properties can be found by opening the ASCII FBX files in a text editor.

        //And FBXHeaderExtension/SceneInfo inside FBX file will be mapped to Scene.AssetInfo

		Scene scene = new Scene(@"test.fbx");

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("DefaultCamera"));

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("UpAxis"));

        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("FrontAxis"));

{{< /highlight >}}
#### **Added ancancellationToken في pen القلم/Sطرق ave:**
**Old Methods:**

{{< highlight "java" >}}

 		public void Open(System.IO.Stream stream, Aspose.ThreeD.FileFormat format)

        public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options)

        public void Open(System.IO.Stream stream)

        public void Open(string fileName, Aspose.ThreeD.FileFormat format)

        public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options)

        public void Open(string fileName)

        public void Save(System.IO.Stream stream, Aspose.ThreeD.FileFormat format)

        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options)

        public void Save(string fileName, Aspose.ThreeD.FileFormat format)

        public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options)

{{< /highlight >}}

**طرق ew ew:**

{{< highlight "java" >}}

         public void Open(System.IO.Stream stream, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(System.IO.Stream stream, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(string fileName, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Open(string fileName, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(System.IO.Stream stream, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(string fileName, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

        public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

{{< /highlight >}}

سوف All فتح/حفظ الطرق لديها معلمة إلغاء إضافية مع قيمة افتراضية ، لذلك الرموز التي تستخدم هذه الأساليب لا تحتاج إلى تعديل لتجميع.

You يمكن استخدام ancancellationTokenSource لإلغاء مهمة حفظ/فتح في أي وقت تحتاج إليه.

**Sوافرة oode:**

{{< highlight "java" >}}

         CancellationTokenSource cts = new CancellationTokenSource();

        Scene scene = new Scene();

        cts.CancelAfter(1000);

        try

        {

                scene.Open("test.fbx", cts.Token);

                Console.WriteLine("Import is done within 1000ms");

        }

        catch (ImportException e)

        {

                if (e.InnerException is OperationCanceledException)

                {

                        Console.WriteLine("It takes too long time to import, and we have canceled the importing.");

                }

        }

{{< /highlight >}}
