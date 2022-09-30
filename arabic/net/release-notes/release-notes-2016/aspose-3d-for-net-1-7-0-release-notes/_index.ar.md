---
title: Aspose.3D for .NET 1.7.0 tes elease oأوتس
type: docs
weight: 60
url: /ar/net/aspose-3d-for-net-1-7-0-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 1.7.0](https://www.nuget.org/packages/Aspose.3D/1.7.0)

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-141|دعم dd dd لتحويل STL إلى تنسيق صورة.|New eature|
|THREEDNET-169|Rأندر المشهد إلى نسيج.|New eature|
|THREEDNET-170|Add دعم الظل.|New eature|
|THREEDNET-174|Gنشيط البيانات العادية من مجموعة التنعيم.|New eature|
|THREEDNET-179|وقعت Index من خطأ النطاق عند تحميل ملف U3D.|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See القائمة لأي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Adds Aspose.ThreeD. nntities. فئة rurustum**
يتم إضافة A فئة جديدة rurustum. كانت amamera و ight ight الطبقات الفرعية من فئة Entity. In الإصدار 1.7.0 ، يتم inherهذه الطبقات من rurustum و rurustum من Entity ، حيث يتم استخراج خصائص sition osition ، Up ، ooookAt ، Direction ، ararget ، lane earPlane و FarPlane في rurustum.
#### **Adds Aspose.ThreeD. فئة مستحضرات التجميل**
يسمح It للمطورين بتعيين خيارات تقديم مختلفة مثل لون الخلفية ودليل الأصول وتمكين/تعطيل ظلال الكائن قبل تحويل ملف 3D إلى صورة.
#### **Adds طرق متعددة Rفي Aspose.ThreeD.Scene الفئة**
It يجعل مشهد 3D في منظور الكاميرا معين في تنسيق ملف الصورة المحدد والحجم.
#### **Adds MoveFطريقة orward في Aspose.ThreeD. nntities. Camera الفئة**
It يتحرك إلى الأمام الكاميرا نحو اتجاهها. يتم تحديد اتجاه الكاميرا A من قبل أي من ararget/Direction/ooookAt

- **Target:**A الهدف عقدة في الفضاء ، فإن الكاميرا ننظر دائما إلى هذا الهدف مهما كان الهدف/الكاميرا قد غيرت موقعها في الفضاء.
- **LookAt:**A موقف ثابت في الفضاء ، فإن الكاميرا ننظر دائما في هذا الموقف.
- **Direction:**A اتجاه ناقلات ، يتم تحديد اتجاه الكاميرا مباشرة من قبل هذا ناقلات مهما كان موقفها.
#### **أعضاء في Aspose.ThreeD. nntities. class eometry الفئة**
يمكن formats تنسيقات ملفات ome تخزين إعدادات الظل ذات الصلة في الهندسة مثل FBX ، كما أنها تستخدم في تقديم.
#### **Adds enerenerateNطريقة أورمال في Aspose.ThreeD. nntities.**
It يسمح للمطورين لتوليد البيانات العادية من Mesh على سبيل المثال ، إذا تم تعريف عنصر mooertexEleالقابل moomoothingGroup على الشبكة ، فإن البيانات العادية التي تم إنشاؤها سوف تحصل على تمهيد من قبل erertexEleالقابل moomoothingGroup.
#### **طريقة ondds ononcate في Aspose.ThreeD.**
It يسمح للمطورين لربط اثنين من التحول دوران إلى واحد ممثلة في Quaternion.
