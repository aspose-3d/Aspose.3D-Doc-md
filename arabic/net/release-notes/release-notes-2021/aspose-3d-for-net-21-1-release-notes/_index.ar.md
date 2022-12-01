---
title: Aspose.3D for .NET 21.1 tes elease ootes
type: docs
weight: 12
url: /ar/net/aspose-3d-for-net-21-1-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 21.1.

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

### Added الفئة Aspose.ThreeD. ender اندر. IenenderQueue

سيتم تمرير مثيل An IenenderQueue إلى enntityRenderer عندما يحاول renderer تقديم شيء ما ، ستحتاج إلى الإعداد لموارد الأجهزة المستخدمة لتقديم وإضافة مهام تقديم إلى قائمة الانتظار في quentityRenderer.


### Rالرموز التعبيرية الفئة Aspose.ThreeD. ender اندر. Ienقابلة للشحن

Tله هو واجهة obsoleted وكان مفيدا لفترة طويلة ، انها آمنة لإزالة هذا.


### Added أعضاء جدد إلى الفئة Aspose.ThreeD.FileFormat:

{{< highlight "csharp" >}}

        /// <summary>
        /// Gets the extension names of this type.
        /// </summary>
        public string[]Extensions{ get;}

        /// <summary>
        /// Universal Scene Description
        /// </summary>
        public static readonly Aspose.ThreeD.FileFormat USD;
{{< /highlight >}}

Formats أشكال ome مثل USD ، GLTF قد يحتوي على أكثر من ملحقات واحدة ، قدمنا خاصية جديدة للحصول على جميع الإضافات.


### Refactored الفئة Aspose.ThreeD. ender اندر. nntityRenderer:

{{< highlight "csharp" >}}
        public void PrepareRenderQueue(Aspose.ThreeD.Render.Renderer renderer, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
{{< /highlight >}}

Hكما تم changed إلى وظيفتين:

{{< highlight "csharp" >}}
        /// <summary>
        /// Prepare rendering commands for specified node/entity pair.
        /// </summary>
        /// <param name="renderer">The current renderer instance</param>
        /// <param name="queue">The render queue used to manage render tasks</param>
        /// <param name="node">Current node</param>
        /// <param name="entity">The entity that need to be rendered</param>
        public void PrepareRenderQueue(Aspose.ThreeD.Render.Renderer renderer, Aspose.ThreeD.Render.IRenderQueue queue, Aspose.ThreeD.Node node, Aspose.ThreeD.Entity entity)
        /// <summary>
        /// Each render task pushed to the <see cref="IRenderQueue"/> will have a corresponding RenderEntity call
        /// to perform the concrete rendering job.
        /// </summary>
        /// <param name="renderer">The renderer</param>
        /// <param name="commandList">The commandList used to record the rendering commands</param>
        /// <param name="node">The same node that passed to PrepareRenderQueue of the entity that will be rendered </param>
        /// <param name="renderableResource">The custom object that passed to IRenderQueue during the PrepareRenderQueue </param>
        /// <param name="subEntity">The index of the sub entity that passed to IRenderQueue</param>
        public virtual void RenderEntity(Renderer renderer, ICommandList commandList, Node node, object renderableResource, int subEntity);
{{< /highlight >}}

في التنفيذ القديم ، قد تسبب موارد الأجهزة المستخدمة عن طريق تقديم تم إنشاؤها خلال مرحلة إعادة الإرسال في مرحلة ueue ، بعض المشاكل في بعض برامج التشغيل.

So نحن فصل إعداد وتقديم ، وتحسين بعض المخابئ الداخلية.


### عضو Obsoleted إزالتها من الفئة Aspose.ThreeD.


{{< highlight "csharp" >}}

        public Aspose.ThreeD.Render.IRenderWindow CreateRenderWindow(Aspose.ThreeD.Render.RenderParameters parameters, System.IntPtr handle)

{{< /highlight >}}

Tكان من المقرر إزالة له ، وهذه وظيفة obsoleted لديه بديل مع نفس الاسم.

