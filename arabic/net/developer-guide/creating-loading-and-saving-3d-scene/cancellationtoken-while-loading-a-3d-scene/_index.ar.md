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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            CancellationTokenSource cts = new CancellationTokenSource();
            Scene scene = new Scene();
            cts.CancelAfter(1000);
            try
            {
                scene.Open("document.fbx" , cts.Token);
                Console.WriteLine("Import is done within 1000ms");
            }
            catch (ImportException e)
            {
                if (e.InnerException is OperationCanceledException)
                {
                    Console.WriteLine("It takes too long time to import, import has been canceled.");
                }
            }

{{< /highlight >}}
