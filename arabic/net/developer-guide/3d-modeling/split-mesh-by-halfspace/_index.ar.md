---
title:"كيفية تقسيم الشبكة باستخدام HalfSpace في Aspose.3D"
type: docs
linkTitle: "Split Mesh by HalfSpace"
description: "تعلم كيفية تقسيم الشبكات ثلاثية الأبعاد باستخدام مستويات HalfSpace في Aspose.3D"
weight: 10
---

# تقسيم الشبكات باستخدام مستويات نصف الفضاء في Aspose.3D

توضح هذه الدروس كيفية استخدام Aspose.3D لإجراء عمليات تقسيم الشبكة باستخدام مستويات نصف الفضاء. تُعد هذه التقنية مفيدة لاستخراج أجزاء محددة من نموذج ثلاثي الأبعاد بناءً على معايير مكانية.

## فهم عمليات نصف الفضاء

يمثل نصف الفضاء مساحة لانهائية مقسمة بمستوى. عند دمجها مع عمليات Aspose.3D المنطقية، تسمح لك باستخراج أجزاء محددة من الشبكة موجودة على جانب واحد من المستوى المحدد.

### المفاهيم الرئيسية:
- **نصف الفضاء**: يمثل مساحة لانهائية مقسمة بمستوى
- **العمليات المنطقية**: تُستخدم لاستخراج أجزاء الشبكة بالنسبة إلى نصف الفضاء
- **معادلة المستوى**: معرفة على أنها ax + by + cz + d = 0، حيث (a، b، c) هو متجه الوحدة
- **الجانب الموجب**: الجزء من الفضاء حيث يشير متجه الوحدة للمستوى

## مثال التعليمات البرمجية: تقسيم شبكة باستخدام نصف فضاء

يوضح الكود التالي بلغة C# كيفية إنشاء شبكة مكعبة بسيطة وتقسيمها باستخدام مستوى نصف فضاء:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // إنشاء مشهد ثلاثي الأبعاد جديد
        Scene scene = new Scene();
        
        // إنشاء شبكة مكعبة (أبعاد 2x2x2 افتراضيًا)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // إنشاء نصف فضاء للقطع
        HalfSpace halfSpace = new HalfSpace();
        
        // تحديد معادلة المستوى: ax + by + cz + d = 0
        // باستخدام متجه الوحدة للمستوى يشير في اتجاه Z
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // تحديد موضع نصف الفضاء (إنشاء عقدة وتحويل)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // تحديد الموضع عند z=0.5
        
        // تنفيذ عملية التقسيم المنطقية
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // إضافة النتيجة إلى المشهد وحفظها
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("تم تقسيم الشبكة باستخدام نصف فضاء بنجاح.");
    }
}
```

## شرح الكود

### متطلبات مساحة الاسم
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // يحتوي على فئات HalfSpace و BooleanOperator
using Aspose.ThreeD.Utilities; // يحتوي على Vector3 و Plane utilities
```

### إنشاء الهندسة
1. **تهيئة المشهد**: `Scene scene = new Scene();`
2. **إنشاء مكعب**: `(new Box()).ToMesh()` ينشئ مكعبًا قياسيًا
3. **التسلسل الهرمي للعقد**: تتم إضافة الشبكة إلى المشهد من خلال عقدة فرعية

### تحديد مستوى القطع
1. **تحديد المستوى**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - ينشئ مستوى XY أفقيًا عند z=0
   - يشير متجه الوحدة (0،0،1) إلى الأعلى

2. **التحديد الموضعي**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - ينقل مستوى القطع إلى z=0.5
   - يؤثر على الجزء الذي سيتم الاحتفاظ به من الشبكة

### تنفيذ العملية
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- يُرجع الجزء من الشبكة على الجانب الموجب من المستوى
- تتم إضافة النتيجة مرة أخرى إلى التسلسل الهرمي للمشهد

### حفظ النتيجة
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- التنسيقات المدعومة تتضمن OBJ و STL و FBX و GLTF والمزيد
- يتم حفظ جزء التقسيم فقط، وليس الشبكة الأصلية

## تصور العملية

### أبعاد الصندوق الأصلية:
- يمتد من (-1,-1,-1) إلى (1,1,1)
- يقع في الأصل

### مع المستوى عند z=0.5:
- يحتفظ بالجزء حيث z > 0.5 (الجزء العلوي من الصندوق)
- يتخلى عن الجزء حيث z < 0.5 (الجزء السفلي من الصندوق)

## الاستخدام المتقدم

### الحصول على جانبي القطع
```csharp
// التقسيم الأصلي (الجانب الموجب)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// عكس المستوى للجانب السالب
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### تعديل مستوى القطع
```csharp
// اتجاه مختلف - قطع مائل
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

يوضح هذا التنفيذ الوظائف الأساسية لقدرات Aspose.3D لتقسيم الشبكة باستخدام مستويات نصف الفضاء، مما يسمح باستخراج دقيق للهندسة ثلاثية الأبعاد بناءً على معايير مكانية.
