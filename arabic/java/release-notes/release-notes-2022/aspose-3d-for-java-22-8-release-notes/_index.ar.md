---
title: Aspose.3D for Java 22.8 tes elease ootes
type: docs
weight: 5
url: /ar/java/aspose-3d-for-java-22-8-release-notes/
description: Tانه الافراج عن الملاحظات من Aspose.3D for Java 22.8.
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 22.8.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-1175 |Fix الافراج عن قضايا ملف الحزمة.|Ask اسأل|
|THREEDNET-1183 |Fix دليل التثبيت الافتراضي لحزمة MSI|Ask اسأل|
|THREEDNET-1176 |لا يمكن التعامل مع ode مع الترجمة الهندسية بشكل صحيح في مصدر USDZ.|تحديد g ug|
|THREEDNET-1179 |Aspose.3D 22.5: xcxception عند محاولة تحميل ملف rml V|تحديد g ug|
|THREEDNET-1181 |Aspose.3D 22.5: Cannot تحويل USD إلى 3DS|تحديد g ug|
|THREEDNET-1184 |XcccessViolationException على بعض الملفات GLTF.|تحديد g ug|
|THREEDNET-1186 |Add مخصص xform مشغل الدعم في USD/USDZ المستورد|حركة بلا حدود|
|THREEDNET-1187 |لا تعمل شركة ateraterial في ملف USD/USDZ.|تحديد g ug|
|THREEDNET-1188 |لا يتم تصدير سمات المواد Mعندما لا نسيج المرفقة|تحديد g ug|
|THREEDNET-1189 |Models تحويلها من FBX إلى USDZ كلها سوداء|تحديد g ug|
|THREEDNET-1190 |Add ateraterialConverter ل USD/USDZ المصدر|حركة بلا حدود|
|THREEDNET-1191 |Viewer رمي استثناء عندما اثنين من البدائية تعلق على عقدة واحدة.|تحديد g ug|
|THREEDNET-1192 |XcnitializationEالإضاءة أثناء بدء نافذة تقديم|تحديد g ug|
|THREEDNET-1194 |FBX xcxceptions: Tأعطى مفتاح "OSL" لم يكن موجودا في القاموس|تحديد g ug|
|THREEDNET-1195 |GLTF Exception: لم تكن سلسلة nplace في شكل صحيح.|تحديد g ug|
|THREEDNET-1196 |GLTF Exception: Aspose.ThreeD. tilitailties. nexnexpected okenException: 'Unexpected رمز 'NaN''|تحديد g ug|
|THREEDNET-1197 |GLTF منع الحمل: Syالجذعية. rrgumentException: 'تم إضافة عنصر n مع نفس المفتاح بالفعل. Key: pcInfoFieldameame'|تحديد g ug|
|THREEDNET-1198 |FBX Exception: Aspose.ThreeD.ImportException: 'Illaw خاصية MultiLayer بينما deserAspose.ThreeD. nntities. NullNode Armature'|تحديد g ug|
|THREEDNET-1199 |FBX منع الحمل: Syالجذعية.|تحديد g ug|
|THREEDNET-1200 |USD Exception: لا يتم دعم Data نوع sdsdTimeCode|تحديد g ug|
|THREEDNET-1201 |USD Exception: لا يتم تنفيذ sdsdQuatf.|تحديد g ug|
|THREEDNET-1202 |USD عدم التسليم: لا يتم دعم sdsdVec3h|تحديد g ug|
|THREEDNET-1203 |USD Exception: لا يتم تنفيذ نوع القاموس غير المبطنة|تحديد g ug|
|THREEDNET-1204 |USD Exception: لا يتم دعم ecec2d|تحديد g ug|
|THREEDNET-1205 |USD Exception: Cannot فتح هذا الملف|تحديد g ug|
|THREEDNET-1206 |USD Exception: Dمحدد SdfPath|تحديد g ug|
|THREEDNET-1207 |USD عدم التسليم: xformOp: لا يتم دعم الشرق.|تحديد g ug|
|THREEDNET-1208 |لا يعمل جهاز التشفير draco من E.|تحديد g ug|
|THREEDNET-1209 |DAE Save إلى USD xcxception: Syالجذعية. nndexOutOfRangeException: "كان Index خارج حدود المصفوفة.|تحديد g ug|


Tversion إصلاح مجموعة من الأخطاء وليس لديها تغييرات رئيسية API.

## API التغييرات ##


### Added طرق جديدة في الفئة `com.aspose.threed.UsdSaveOptions`:

{{< highlight "java" >}}
    /**
     * Custom converter to convert the geometry's material to PBR material
     * If this is unassigned, USD exporter will automatically convert the standard material to PBR material.
     * Default value is null
     */
    public MaterialConverter getMaterialConverter();
    /**
     * Custom converter to convert the geometry's material to PBR material
     * If this is unassigned, USD exporter will automatically convert the standard material to PBR material.
     * Default value is null
     * @param value New value
     */
    public void setMaterialConverter(MaterialConverter value);
{{< /highlight >}}



Aspose.3D لديه المدمج في التنفيذ لتحويل غير PBR المواد إلى PBR المواد ل glTF/USD/USD الأشكال ، ولكن نحن أيضا توفير تنفيذ مخصص لإجراء التحويل.



### Roroperties تحديث لدعم جديد FBX تعريفات المواد:

Old definitions:

{{< highlight "csharp" >}}
    /**
     * Gets the shader language used by this technique.
     */
    public ShadingLanguage getShaderLanguage();
    
    /**
     * Sets the shader language used by this technique.
     * @param value New value
     */
    public void setShaderLanguage(ShadingLanguage value);
    /**
     * Gets the rendering API used by this technique
     */
    public RenderingAPI getRenderAPI();
    
    /**
     * Sets the rendering API used by this technique
     * @param value New value
     */
    public void setRenderAPI(RenderingAPI value);
{{< /highlight >}}

تعريفات ew ew:

{{< highlight "java" >}}
    /**
     * Gets the shader language used by this technique.
     */
    public String getShaderLanguage();
    
    /**
     * Sets the shader language used by this technique.
     * @param value New value
     */
    public void setShaderLanguage(String value);
    /**
     * Gets the rendering API used by this technique
     */
    public String getRenderAPI();
    
    /**
     * Sets the rendering API used by this technique
     * @param value New value
     */
    public void setRenderAPI(String value);
{{< /highlight >}}
		
		




