---
title: Aspose.3D for .NET 1.5.0 tes elease oأوتس
type: docs
weight: 80
url: /ar/net/aspose-3d-for-net-1-5-0-release-notes/
---
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key** |**Sأوماري** |**Category** |
|:- |:- |:- |
|THREEDNET-146 |Geomeonvert هندسي إلى هيكل القشرة الواحدة.|New eature|
|THREEDNET-148 |Aمنخفض المستخدم إلى تقسيم شبكة لكل المواد.|New eature|
|THREEDNET-150 |Cشبكة reate للطائرة.|New eature|
|THREEDNET-151 |Cشبكة reate ل ox ox.|New eature|
|THREEDNET-152 |شبكة rereate ل Sphere.|New eature|
|THREEDNET-153 |Cشبكة reate للاسطوانة.|New eature|
|THREEDNET-155 |Create شبكة لتوروس.|New eature|
|THREEDNET-145 |Allow الوجه تنسيق النظام في U3D تحميل/حفظ فئة التكوين.|Enhancement|
|THREEDNET-154 |Sقضية بيل: Distreet3DS يجب أن يكون Discreet3DS.|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See القائمة لأي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Emoemoval من تنسيق Distreet3D.**
يتم وضع علامة تنسيق Distreet3Dكما عفا عليها الزمن بسبب موجة غير صحيحة.
#### **Adds Discreet3DS التنسيق.**
Discreet3DS تم تقديم شكل.
#### **واجهة Adds Aspose.ThreeD. nntities.**
يمكن تحويل فئة ny ny التي تنفذ هذه الواجهة إلى mesh أثناء التصدير إلى أي تنسيقات ملفات 3D.
#### **Adds الفئة Aspose.ThreeD. nntities.**
It مشتق من فئة Entity وأيضا الطبقة الأساسية لجميع الطبقات البدائية.
#### **Adds الفئة Aspose.ThreeD. nntities. ox ox/Cيندر/lane لين/Sفير/Torus**
These يمكن استخدامها لتحديد المشهد مع البدائية بسيطة. Dإيفلين يمكن أيضا تحويلها إلى شبكة تلقائيا.
#### **Adds فئة Aspose.ThreeD. nntities. TriMesh/TriMesh<T>**
Tريبليش/Tريبليش<T>يحتوي على تعريف الشبكات القائمة على المثلث مع تخطيط الذاكرة المخصصة ، وهو أمر مفيد عندما يتطلب المطور لتحويل المشهد إلى تنسيقات الملفات الخاصة بهم أو في تقديم.
#### **هيكل Adds Aspose.ThreeD. tiliتيليتيز. Fecector2/FVector3/Fecector4**
الطبقات These الحاضر مكونات ناقلات في تعويم. Only عدد قليل من vector الحديثة vector U يدعم ناقلات مزدوجة الدقة ، وأنواع تعويم واحدة الدقة هي أكثر الترحيب في الوقت الحقيقي تقديم العالم. سوف تتعايش بدائل ese hese مع الأصلي Vector2/Vector3/Vector4 لأنها تلعب أدوار مختلفة في Aspose.3D. يستخدم ououble-الدقة أساسا لتخزين بيانات النموذج لأنه يحتوي على خطأ أقل تراكمًا. يتم استخدام Single-الدقة بشكل رئيسي في تقديم أو تحويل تنسيقات الملفات الخاصة بالمستخدم لأنه يحتوي على قبول وأداء أفضل. قدم We هذه المجموعة من ناقلات في Aspose.3D 1.5 لأننا أضفنا الدعم لتخطيط فيرتكس مخصص ، حيث سيتم استخدام ناقلات تعويم بشكل متكرر.
#### **Attribudds سمة الفئة Aspose.ThreeD. tiliتيليتيز.**
Dإيفلوبر يمكن تحديد هيكل مخصص ل فيرتكس ، واستخدام هذه السمة للاحتفال الدلالية من الحقول.
#### **Adds الفئة Aspose.ThreeD. tiliتيليتيز.**
It يصف تخطيط الذاكرة من قمة الرأس.
#### **Adds enum Aspose.ThreeD.**
أنواع These enum توضح نوع بيانات حقل فيرتكس والدلالية على التوالي.
#### **Adds الفئة Aspose.ThreeD. tiliتيليتيز.**
يصف It كل حقل في تخطيط الذاكرة المخصص لـ erertex.
#### **Adds الفئة Aspose.ThreeD. tiliتيليتيز. erertex**
يمكن استخدام It للوصول إلى القشرة الخام في TriMesh/TriMesh<T>
#### **Adds enum Aspose.ThreeD. nntities. plplitMeshPolicy**
It يحدد سياسة البيانات المستخدمة في خوارزمية تقسيم الشبكة ، ونحن نؤيد اثنين من السياسات ، وتبادل البيانات بين الشبكات الفرعية أو كل شبكة فرعية لديها البيانات الخاصة بها (Oالبيانات المستخدمة nly).
#### **Adds 3 طرق plplitMesh إلى Aspose.ThreeD. nntities.**
1. تنسجم lit plit على عقدة محددة إلى شبكات فرعية حسب التعريف المادي.
1. Split كل شبكة في المشهد معين إلى الشبكات الفرعية حسب التعريف المادي.
1. Split شبكة معينة إلى الشبكات الفرعية حسب التعريف المادي.
#### **Property dds خاصية liplipCotrademateSyالجذعية في الفئة Aspose.ThreeD. orormat. Universal3Dononfig**
It يسمح للمستخدمين flip نظام التنسيق من U3D أثناء الاستيراد أو التصدير.

