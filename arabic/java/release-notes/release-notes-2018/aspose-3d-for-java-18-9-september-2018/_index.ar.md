---
title: Aspose.3D for Java 18.9-سبتمبر 2018
type: docs
weight: 40
url: /ar/java/aspose-3d-for-java-18-9-september-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 18.9](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.9/).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Sأوماري**|**Category**|
|:- |:- |
|CanellationTدعم أوكين|New eature|
|FBX ExportException-Hhigh olyأوليغون Count|Bug|
|ImportException أثناء فتح ملفات ضخمة FBX|Bug|
|يتم تحميل جميع الخصائص من FBX الإعدادات العالمية في AssetInfo|Bug|

## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**

Pالإيجار عرض قائمة أي تغييرات أجريت على الجمهور API مثل إضافة ، إعادة تسميتها ، إزالة أو استبعاد الأعضاء وكذلك أي تغيير متوافق غير متخلف المحرز إلى Aspose.3D for Java API. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).

## **API التغييرات:**

**Cلاس com.aspose.threed. added ode وأضاف 2 طرق جديدة:**

{{< highlight "java" >}}

     /**

     * Per-node asset info

     * @param value New value

     */

    public void setAssetInfo(com.aspose.threed.AssetInfo);

    /**

     * Per-node asset info

     */

    public com.aspose.threed.AssetInfo getAssetInfo();

{{< /highlight >}}


يمكن أن تتضمن أنواع ملفات ome معلومات الأصول لكل عقدة.
In FBX ، خاصية AssetInfo من عقدة الجذر تحتوي على الإعدادات العالمية المحددة في الملفات FBX.



**Sوافرة oode:**

{{< highlight "java" >}}

         //Access GlobalSettings in FBX file, more properties can be found by opening the ASCII FBX files in a text editor.

        //And FBXHeaderExtension/SceneInfo inside FBX file will be mapped to Scene.AssetInfo

        Scene scene = new Scene("test.fbx");

        AssetInfo globalSettings = scene.getRootNode().getAssetInfo();

        System.out.println(globalSettings.getProperty("DefaultCamera"));

        System.out.println(globalSettings.getProperty("UpAxis"));

        System.out.println(globalSettings.getProperty("FrontAxis"));

{{< /highlight >}}

**تم إضافة 10 طرق جديدة:**

These كلها أعباء جديدة إلى طرق الحفظ/الفتح الأصلية:

**Old Methods:**

{{< highlight "java" >}}

     /**

     * Opens the scene from given stream using specified file format.

     * @param stream Input stream, user is responsible for closing the stream.

     * @param format File format.

     * @param cancellationToken Cancellation token to the load task

     */

    public void open(Stream stream, FileFormat format, Cancellation cancellationToken)

        throws ImportException;

    /**

     * Opens the scene from given stream using specified IO config.

     * @param stream Input stream, user is responsible for closing the stream.

     * @param options More detailed configuration to open the stream.

     * @param cancellationToken Cancellation token to the load task

     */

    public void open(Stream stream, LoadOptions options, Cancellation cancellationToken)

        throws ImportException;

    /**

     * Opens the scene from given stream

     * @param stream Input stream, user is responsible for closing the stream.

     * @param cancellationToken Cancellation token to the load task

     */

    public void open(Stream stream, Cancellation cancellationToken)

        throws IOException;

    /**

     * Opens the scene from given path using specified file format.

     * @param fileName File name.

     * @param format File format.

     * @param cancellationToken Cancellation token to the load task

     */

    public void open(String fileName, FileFormat format, Cancellation cancellationToken)

        throws IOException;

    /**

     * Opens the scene from given path using specified file format.

     * @param fileName File name.

     * @param options More detailed configuration to open the stream.

     * @param cancellationToken Cancellation token to the load task

     */

    public void open(String fileName, LoadOptions options, Cancellation cancellationToken)

        throws IOException;

    /**

     * Opens the scene from given path

     * @param fileName File name.

     * @param cancellationToken Cancellation token to the load task

     */

    public void open(String fileName, Cancellation cancellationToken)

        throws IOException;

    /**

     * Saves the scene to stream using specified file format.

     * @param stream Input stream, user is responsible for closing the stream.

     * @param format Format.

     * @param cancellationToken Cancellation token to the save task

     */

    public void save(Stream stream, FileFormat format, Cancellation cancellationToken)

        throws ExportException;

    /**

     * Saves the scene to stream using specified file format.

     * @param stream Input stream, user is responsible for closing the stream.

     * @param options More detailed configuration to save the stream.

     * @param cancellationToken Cancellation token to the save task

     */

    public void save(Stream stream, SaveOptions options, Cancellation cancellationToken)

        throws ExportException;

    /**

     * Saves the scene to specified path using specified file format.

     * @param fileName File name.

     * @param format Format.

     * @param cancellationToken Cancellation token to the save task

     */

    public void save(String fileName, FileFormat format, Cancellation cancellationToken)

        throws IOException;

    /**

     * Saves the scene to specified path using specified file format.

     * @param fileName File name.

     * @param options More detailed configuration to save the stream.

     * @param cancellationToken Cancellation token to the save task

     */

    public void save(String fileName, SaveOptions options, Cancellation cancellationToken)

        throws IOException;

{{< /highlight >}}

You يمكن استخدام تسمية Cلإلغاء مهمة حفظ/فتح في أي وقت تحتاجه.

**Sوافرة oode:**

{{< highlight "java" >}}

         final Cancellation cts = new Cancellation();

        Thread thread = new Thread(() -> {

            try {

                Thread.sleep(1000);

                cts.cancel();

            } catch(InterruptedException e) {

                throw new RuntimeException(e);

            }

        });

        thread.start();

        Scene scene = new Scene();

        try {

            scene.open("test.fbx", cts);

            System.out.println("Import is done within 1000ms");

        } catch(ImportException e) {

            if(e.getCause() instanceof CancellationException) {

                System.out.println("It takes too long time to import, and we have canceled the importing.");

            }

        }

{{< /highlight >}}

