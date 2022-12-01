---
title: CancellationToken أثناء تحميل مشهد 3D في C#
linktitle: CancellationToken أثناء تحميل مشهد 3D
type: docs
weight: 80
url: /ar/net/cancellationtoken-while-loading-a-3d-scene/
description: You يمكن استخدام ancancellationTokenSource لإلغاء مهمة حفظ/فتح في أي وقت تحتاج مع C# 3D ملف التلاعب وتحويل API.
---
## **CancellationToken أثناء تحميل مشهد 3D**
سوف All فتح/حفظ الطرق لديها معلمة إلغاء إضافية مع قيمة افتراضية ، لذلك الرموز التي تستخدم هذه الأساليب لا تحتاج إلى تعديل لتجميع.

You يمكن استخدام `CancellationTokenSource` لإلغاء مهمة الحفظ/الفتح في أي وقت تحتاجه ، كما هو موضح في هذا C# رمز المثال مع C# 3D تنسيقات الملفات التلاعب API:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
