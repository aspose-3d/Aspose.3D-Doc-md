---
title: Aspose.3D for Java 20.8 tes elease ootes
type: docs
weight: 9
url: /ar/java/aspose-3d-for-java-20-8-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 20.8.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-698|دعم Added من استيراد ملفات ثلاثية الأبعاد مضغوط|
|THREEDNET-697|لم يتم دعم مواد ixixed ixR مع مميزة في GLTF|
|THREEDNET-705|Added FBX 6.0 دعم الاستيراد|
|THREEDNET-706|Added FBX 6.1 دعم الاستيراد|
|THREEDNET-707|Added FBX 7.0/7.1 دعم الاستيراد|
|THREEDNET-708|لا يتم دعم السمات غير المدعومة في FBX.|
|THREEDNET-703|Added FBX 7.7 دعم الاستيراد|
|THREEDNET-704|OBJ ملف مع مؤشر العنصر السلبي غير معتمد.|
|THREEDNET-700|Fixed Aspose.3D معلقة في تحليل ملف غير مكتمل PDF|
|THREEDNET-699|Fixed Aspose.3D العادم جميع الذاكرة عند تحليل بعض ملف PDF|
|THREEDNET-714|Aspose.3D يأخذ الكثير من الذاكرة و CPU لتحميل ملف GLB|
|THREEDNET-715|Ixixed تجعل شبكة بسيطة (مع البيانات العادية فقط) مع المواد PBR غير صحيحة|
|THREEDNET-711|Aspose.3D معلقة عند استيراد ملف FBX.|
|THREEDNET-710|لا يعمل dering enتحت بعض الأجهزة AD D.|

## API التغييرات ##
Tنسخته هي أساسا نسخة إصلاح الأخطاء ، لذلك لا عينات رمز.

### Added Classes ###
  * الفئة com.aspose.threed. brbrSpecularial aterial-يستخدم في تمثيل مادة pbr المضاربة ، في الوقت الحالي فقط في GLTF 2.0.
  * Added الفئة com.Aspose.threed.VertexElementHole-لدعم ثقب في شبكة FBX
### Added emالجمر ###
  * عضو Added إلى نوع enum com.aspose.threed.
```
public static final com.aspose.threed.VertexElementType Hole;
```
  * أعضاء Added إلى الفئة com.aspose.threed. ilileFormat
```
public static final com.aspose.threed.FileFormat ZIP;
```
Wث هذا الدعم تنسيق ملف جديد ، Aspose.3D يمكن استيراد ملف الرمز البريدي الذي يحتوي على ملف 3D. Usually لا تحتاج إلى استخدام هذا يدويا.

