---
title: Aspose.3D for Java 21.1 tes elease ootes
type: docs
weight: 12
url: /ar/java/aspose-3d-for-java-21-1-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 21.1.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-784 |Add دعم تنسيق Udd dd dd|ميزة ew ew|
|THREEDNET-773 |Add دعم المواد لملف DXF|حركة بلا حدود|
|THREEDNET-797 |دعم dd dd ل. صافي 5.0|حركة بلا حدود|
|THREEDNET-803 |Improof omomboBox في بائع الويب.|حركة بلا حدود|
|THREEDNET-795 |Obj لتحويل uثلاثية الأبعاد-نسيج مفقود|إصلاح g ug|
|THREEDNET-801 |Tانه تنفيذ الإسقاط التقويمي الكاميرا غير صحيح|إصلاح g ug|
|THREEDNET-783 |Map bitmap إلى مثلثات من GLB.|إصلاح g ug|
|THREEDNET-802 |Draco/glTF Fسوف تستخدم خوارزمية درجة التنبؤ فشل في الاستيراد.|إصلاح g ug|
|THREEDNET-804 |Aspose.3D تقديم لا يعمل على بعض المتكاملة GPU|إصلاح g ug|



## API التغييرات ##

Tهنا اثنين من التغييرات الرئيسية في 21.1 ،

* تحسين أداء enenderer عن طريق فصل الإعداد وتقديم ، كما إصلاح بعض الأخطاء ذات الصلة تقديم.
* دعم Added من استيراد USimport import

### Added الفئة `com.aspose.threed.IRenderQueue`

سيتم تمرير مثيل An IenenderQueue إلى enntityRenderer عندما يحاول renderer تقديم شيء ما ، ستحتاج إلى الإعداد لموارد الأجهزة المستخدمة لتقديم وإضافة مهام تقديم إلى قائمة الانتظار في quentityRenderer.


{{< highlight "java" >}}
/**
 * Entity renderer uses this queue to manage render tasks.
 */
public interface IRenderQueue
{    
    /**
     * Add render task to the render queue.
     * @param groupId Which group of the queue the render task will be in
     * @param pipeline The pipeline instance used for this render task
     * @param renderableResource Custom object that will be sent to EntityRenderer.RenderEntity
     * @param subEntity The index of sub entities, useful when the entity is consisting of more than one sub renderable components.
     */
    void add(RenderQueueGroupId groupId, IPipeline pipeline, Object renderableResource, int subEntity);
}
{{< /highlight >}}



### Rفئة الرموز `com.aspose.threed.IRenderable`

Tله هو واجهة obsoleted وكان مفيدا لفترة طويلة ، انها آمنة لإزالة هذا.


### Added أعضاء جدد إلى الفئة `com.aspose.threed.FileFormat`:

{{< highlight "java" >}}
    /**
     * Gets the extension name of this type.
     */
    public String[]getExtensions();

    /**
     * Universal Scene Description
     */
    public static final FileFormat USD;

{{< /highlight >}}

Formats أشكال ome مثل USD ، GLTF قد يحتوي على أكثر من ملحقات واحدة ، قدمنا خاصية جديدة للحصول على جميع الإضافات.


### فئة التصنيع الإلكتروني `com.aspose.threed.EntityRenderer`:

{{< highlight "java" >}}
        public void prepareRenderQueue(com.aspose.threed.Render.Renderer renderer, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
{{< /highlight >}}

Hكما تم changed إلى وظيفتين:

{{< highlight "java" >}}

    /**
     * Prepare rendering commands for specified node/entity pair.
     * @param renderer The current renderer instance
     * @param queue The render queue used to manage render tasks
     * @param node Current node
     * @param entity The entity that need to be rendered
     */
    public void prepareRenderQueue(Renderer renderer, IRenderQueue queue, Node node, Entity entity);
    
    /**
     * Each render task pushed to the {@link com.aspose.threed.IRenderQueue} will have a corresponding RenderEntity call
     * to perform the concrete rendering job.
     * @param renderer The renderer
     * @param commandList The commandList used to record the rendering commands
     * @param node The same node that passed to PrepareRenderQueue of the entity that will be rendered
     * @param renderableResource The custom object that passed to IRenderQueue during the PrepareRenderQueue
     * @param subEntity The index of the sub entity that passed to IRenderQueue
     */
    public void renderEntity(Renderer renderer, ICommandList commandList, Node node, Object renderableResource, int subEntity);
{{< /highlight >}}

في التنفيذ القديم ، قد تسبب موارد الأجهزة المستخدمة عن طريق تقديم تم إنشاؤها خلال مرحلة إعادة الإرسال في مرحلة ueue ، بعض المشاكل في بعض برامج التشغيل.

So نحن فصل إعداد وتقديم ، وتحسين بعض المخابئ الداخلية.


### عضو Obsoleted إزالتها من الفئة `com.aspose.threed.RenderFactory`:


{{< highlight "java" >}}

        public com.aspose.threed.IRenderWindow createRenderWindow(com.aspose.threed.RenderParameters parameters, long handle);

{{< /highlight >}}

Tكان من المقرر إزالة له ، وهذه وظيفة obsoleted لديه بديل مع نفس الاسم.

