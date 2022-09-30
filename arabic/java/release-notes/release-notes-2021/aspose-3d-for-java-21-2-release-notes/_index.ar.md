---
title: Aspose.3D for Java 21.2 tes elease ootes
type: docs
weight: 11
url: /ar/java/aspose-3d-for-java-21-2-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 21.2.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-825 |Add USDZ دعم الاستيراد.|ميزة ew ew|
|THREEDNET-824 |Add دعم الملمس في USDZ|Ask اسأل|
|THREEDNET-811 |Implement نسخة التقييم ذات الصلة xcxception في API|حركة بلا حدود|
|THREEDNET-813 |مطلوب تفاصيل Technical على المواد Mو exexture API القيود-API لا يوفر وسيلة لاكتشاف القوام على المواد|حركة بلا حدود|
|THREEDNET-817 |دعم dd dd للبايت الملمس [] في حالة glb ، gltf ، obj|حركة بلا حدود|
|THREEDAPP-80 |Improof سرعة تحميل الصفحة من بائع الويب|حركة بلا حدود|
|THREEDNET-814 |مؤشرات riangle غير صحيحة|إصلاح g ug|
|THREEDNET-809 |FBX Save Exception: نوع السمة غير المدعومة|إصلاح g ug|
|THREEDNET-810 |Filesize هو الحصول على أكبر أثناء إعادة استخدام نفس الملمس|إصلاح g ug|
|THREEDNET-816 |شبكة غير صحيحة أثناء التحميل OBJ|إصلاح g ug|
|THREEDNET-807 |Tهنا لا نسيج في تصدير FBX|إصلاح g ug|
|THREEDNET-815 |المواد Mمع نموذج شادر = سوف فشل غير معروف لتقديم.|إصلاح g ug|
|THREEDNET-823 |Mشبكة ultiple تعلق على نفس العقدة لا تقدم.|إصلاح g ug|
|THREEDNET-647 |Add التحكم في التحجيم I I في بائع الويب.|Ask اسأل|
|THREEDNET-646 |Add دوران التحكم UI في بائع الويب.|Ask اسأل|



## API التغييرات ##

### Added الفئة `com.aspose.threed.TextureSlot`

Tله تعرض فتحات الملمس الداخلي في المواد ، من أجل الوصول إلى جميع فتحات الملمس المتاحة من مادة ، واستخدام لكل بيان:

{{< highlight "java" >}}
        var mat = new PbrMaterial();
        for(var textureSlot : mat) {
            System.out.println(textureSlot.getSlotName());
            System.out.println(textureSlot.getTexture());
        }
{{< /highlight >}}

### Added الفئة `com.aspose.threed.TrialException`

Rom rom 21.2 ، عندما يصل الاستخدام غير المرخص إلى تقييد الترخيص ، سيتم طرح تعليق rialEnotify restriction الترخيص ، وكيفية التقدم بطلب للحصول على ترخيص مؤقت.

You يمكن ببساطة تجاهل هذا عن طريق محاولة تحيط/قبض كتلة على ave ave/Oعملية القلم ، أو إيقاف هذا الاستثناء عن طريق:

{{< highlight "java" >}}
        TrialException.setSuppressTrialException(true);
{{< /highlight >}}

Turn هذه الرسالة قبالة لن ترفع القيود (يتم تجاهل العقد الإضافية ike إيكي من قبل المصدر/المستورد).

In الطلب للحصول على كل ميزة كاملة ، يرجى طلب رخصة مؤقتة أو شراء رخصة ميزة كاملة.

### طرق Added إلى `com.aspose.threed.TriMesh`


{{< highlight "java" >}}
    /**
     * Read the vector4 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector4/FVector4 data type
     */
    public Vector4 readVector4(int idx, VertexField field);
  
    /**
     * Read the vector4 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector4/FVector4 data type
     */
    public FVector4 readFVector4(int idx, VertexField field);
  
      /**
     * Read the vector3 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector3/FVector3 data type
     */
    public Vector3 readVector3(int idx, VertexField field);
    
    /**
     * Read the vector3 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector3/FVector3 data type
     */
    public FVector3 readFVector3(int idx, VertexField field);

  
    /**
     * Read the vector2 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector2/FVector2 data type
     */
    public Vector2 readVector2(int idx, VertexField field);
    
    /**
     * Read the vector2 field
     * @param idx The index of vertex to read
     * @param field The field with a Vector2/FVector2 data type
     */
    public FVector2 readFVector2(int idx, VertexField field);

  
    /**
     * Read the double field
     * @param idx The index of vertex to read
     * @param field The field with a float/double compatible data type
     */
    public double readDouble(int idx, VertexField field);
    
    /**
     * Read the float field
     * @param idx The index of vertex to read
     * @param field The field with a float/double compatible data type
     */
    public float readFloat(int idx, VertexField field);
{{< /highlight >}}


تسمح لك طرق These بقراءة حقل فيرتكس دون تخصيص ذاكرة إضافية ، والطريقة التقليدية للوصول إلى فيرتكس من `TriMesh` تولد في الواقع الكثير من الأشياء المؤقتة ، ويمكن أن توفر إمكانية الوصول إلى بصمة الذاكرة بسرعة ومنخفضة.

{{< highlight "java" >}}
Cencene s = جديد cencene ("test .STL") ؛
Var mesh = (Mesh)s.getRootNode().getChild(0).getEntity() ؛

// Rereate جديد erertexDeclaration ، وبالتالي فإن TriMesh قمنا ببناء في وقت لاحق سوف تستخدم هذا تخطيط الذاكرة.
فار vd = جديد VertexDeclaration() ؛
فار بوس = vd. adFifield (VertexFieldDataType. F_V_TRR3 ، VertexFieldS. emanemanSITON N) ؛
فار عادي = vd. adFifield (VertexFieldDataType. F_V_TRR3 ، VertexFieldS. emanemanRML L) ؛
// إنشاء مثال TriMesh من instance esh مثيل مع إعلان فيرتكس محدد يدويا
فار م = TriMesh. fromMsh (vd ، mesh) ؛
ل (int i = 0; i< m.getVerticesCount(); i++)
        {
            //access each field
            var v_pos = m.readFVector3(i, pos);
            var v_normal = m.readFVector3(i, normal);
            System.out.printf("(%s), (%s)\n", v_pos, v_normal);
        }
{{< /highlight >}}


### Added تنسيق ملف جديد في `com.aspose.threed.FileFormat`

{{< highlight "java" >}}
    /**
     * Compressed Universal Scene Description
     */
    public static final FileFormat USDZ;
{{< /highlight >}}

Aspose.3D 21.2 يمكن تحميل USDZ تنسيق الآن.


### Ixixed غير متسقة APIs:

يتم نقل الطبقات القديمة These إلى حزمة com.aspos.threed.de مستبعدة ، ويتم إدخال فئات جديدة لتحل محلها:

|**Old lass لاس** |**New lass** |
|:- |:- |
|Com. aspose.threed. ptions 3 Dptions ptions aveO|Com. aspose.threed. ptions 3dwSaveOptions|
|Com. aspose.threed. ptions ptions ptions ptions aveO|كوم. أسبوس. ثريد.|
|Com. aspose.threed. isiscreet3Dptions ptions oadO|Com. aspose.threed. ptions iscreet3dsLoadO|
|Com. aspose.threed. isiscreet3Dptions ptions aveO|Com. aspose.threed. ptions iscreet3dsSaveO|
|Com. aspose.threed. ptions ptions ptions ptions oadO|كوم. أسبوس. ثريد.|
|Com. aspose.threed. ptions ptions ptions ptions aveO|Com. aspose.threed. ptions bxSaveO|
|Com. aspose.threed. ptions ptions ptions ptions oadOptions|كوم. أسبوس. ثريد.|
|Com. aspose.threed. ptions ptions ptions ptions ptions aveO|كوم. أسبوس. ثريد.|
|Com. aspose.threed. ptions ptions ptions ptions 5SaveOptions|Com. aspose.threed. ptions tml5SaveO|
|Com. aspose.threed. ptions ptions ptions ptions oadO|كوم. أسبوس. ثريد.|
|Com. aspose.threed. ptions ptions ptions ptions aveO|كوم. أسبوس. ثريد.|
|Com. aspose.threed. ptions 3Dptions oadO|Com. aspose.threed. ptions 3dLoadOptions|


