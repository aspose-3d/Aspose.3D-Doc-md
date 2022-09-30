---
title: Aspose.3D for .NET 22.3 tes elease ootes
type: docs
weight: 10
url: /ar/net/aspose-3d-for-net-22-3-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D for .NET 22.3.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 22.3.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1103 |Improof شبكة كبيرة في U3D/PDF تصدير الملف|حركة بلا حدود|
|THREEDNET-1081 |وظائف simplified dd المبسطة merg|حركة بلا حدود|
|THREEDNET-1077 |Gالطاقة glTF لا يمكن تمرير glTF المدقق عند تمكين ضغط دراكو.|إصلاح g ug|


## API التغييرات ##


### Added طرق ثابتة جديدة إلى الفئة `Aspose.ThreeD.Scene`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Opens the scene from given stream using specified file format.
        /// </summary>
        /// <param name="stream">Input stream, user is responsible for closing the stream.</param>
        /// <param name="format">File format.</param>
        /// <param name="cancellationToken">Cancellation token to the load task</param>
        public static Scene FromStream(Stream stream, FileFormat format, CancellationToken cancellationToken = default(CancellationToken));
        /// <summary>
        /// Opens the scene from given stream using specified IO config.
        /// </summary>
        /// <param name="stream">Input stream, user is responsible for closing the stream.</param>
        /// <param name="options">More detailed configuration to open the stream.</param>
        /// <param name="cancellationToken">Cancellation token to the load task</param>
        public static Scene FromStream(Stream stream, LoadOptions options, CancellationToken cancellationToken = default(CancellationToken));
        /// <summary>
        ///  Opens the scene from given stream
        /// </summary>
        /// <param name="stream">Input stream, user is responsible for closing the stream.</param>
        /// <param name="cancellationToken">Cancellation token to the load task</param>
        public static Scene FromStream(Stream stream, CancellationToken cancellationToken = default(CancellationToken));
{{< /highlight >}}

Overhese الأحمال الزائدة تسمح ببناء مشهد مباشرة من تيار ، مع المزيد من الخيارات الموروثة من `Scene.Open`.

{{< highlight "csharp" >}}
        //Before 22.3, load a scene from stream:
        //var scene = new Scene();
        //scene.Open(stream);

        //Now we load a scene from stream
        var scene = Scene.FromStream(stream);
{{< /highlight >}}


### Added طرق ثابتة جديدة إلى الفئة `Aspose.ThreeD.Scene`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Opens the scene from given path using specified file format.
        /// </summary>
        /// <param name="fileName">File name.</param>
        /// <param name="format">File format.</param>
        /// <param name="cancellationToken">Cancellation token to the load task</param>
        public static Scene FromFile(string fileName, FileFormat format, CancellationToken cancellationToken = default(CancellationToken));

        /// <summary>
        /// Opens the scene from given path using specified file format.
        /// </summary>
        /// <param name="fileName">File name.</param>
        /// <param name="options">More detailed configuration to open the stream.</param>
        /// <param name="cancellationToken">Cancellation token to the load task</param>
        public static Scene FromFile(string fileName, LoadOptions options, CancellationToken cancellationToken = default(CancellationToken));

        /// <summary>
        /// Opens the scene from given path
        /// </summary>
        /// <param name="fileName">File name.</param>
        /// <param name="cancellationToken">Cancellation token to the load task</param>
        public static Scene FromFile(string fileName, CancellationToken cancellationToken = default(CancellationToken));


{{< /highlight >}}

These الأحمال الزائدة تسمح ببناء مشهد مباشرة من اسم الملف ، مع المزيد من الخيارات الموروثة من `Scene.Open`.

تم الآن وضع علامة على منشئ قديم من Scene مع fileName paramter كما obsoleted وسيتم إزالتها في المستقبل.

{{< highlight "csharp" >}}
        //Before 22.3, load a scene from file:
        //var scene = new Scene();
        //scene.Open("fileName");

        //Now we load a scene from file
        var scene = Scene.FromFile("fileName");
{{< /highlight >}}




### Added طرق ثابتة جديدة إلى الفئة `Aspose.ThreeD.Node`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Detach everything under the node and attach them to current node.
        /// </summary>
        /// <param name="node"></param>
        public void Merge(Aspose.ThreeD.Node node);
{{< /highlight >}}


Tأسلوبه الجديد يسمح دمج كل شيء من عقدة أخرى إلى عقدة الحالية.

Sرمز وافرة لدمج file1 و file2:

{{< highlight "csharp" >}}
        var scene1 = Scene.FromFile("file1");
        var scene2 = Scene.FromFile("file2");
        scene1.RootNode.Merge(scene2.RootNode);
        scene1.Save("output.fbx", FileFormat.FBX7700Binary);
{{< /highlight >}}

