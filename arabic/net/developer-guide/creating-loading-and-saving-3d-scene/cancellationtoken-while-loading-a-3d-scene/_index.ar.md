---
title: CancellationToken أثناء تحميل مشهد 3D في C#
linktitle: CancellationToken أثناء تحميل مشهد 3D
type: docs
weight: 80
url: /ar/net/cancellationtoken-while-loading-a-3d-scene/
description: يمكنك استخدام CancellationTokenSource لإلغاء مهمة الحفظ/الفتح في أي وقت تحتاج فيه باستخدام C# 3D معالجة الملفات وتحويلها API.
---
##  **CancellationToken أثناء تحميل مشهد 3D**
سوف All فتح/حفظ الطرق لديها معلمة إلغاء إضافية مع قيمة افتراضية ، لذلك الرموز التي تستخدم هذه الأساليب لا تحتاج إلى تعديل لتجميع.

You can use the `CancellationTokenSource` to cancel the save/open task at any time you need, as shown in this C# code example with C# 3D file formats manipulation API:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
