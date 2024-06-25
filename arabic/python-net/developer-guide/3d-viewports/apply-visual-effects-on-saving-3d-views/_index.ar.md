---
title: تطبيق تأثيرات بصرية على توفير 3D مشاهدة
type: docs
weight: 10
url: /ar/python-net/apply-visual-effects-on-saving-3d-views/
description: باستخدام Aspose.3D for Python via .NET API ، يمكن للمطورين تطبيق تأثيرات بصرية على مشاهدات 3D قبل الحفظ في الصورة. تُعرف هذه التأثيرات المرئية أيضًا بتأثيرات ما بعد المعالجة أو الفلاتر التي يتم تطبيقها في الوقت الفعلي على كل شيء معروض في طريقة العرض 3D.
---
{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), developers may apply visual effects on 3D Views before saving in the image. These visual effects are also known as the post-processing effects or filters those are applied in real-time to everything displayed in the 3D View.

{{% /alert %}}
##  **تطبيق تأثيرات بصرية على عرض 3D**
تسمح طريقة [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) لفئة [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) بإنشاء أي تأثير مرئي مدعوم. فئة `Renderer` تقدم عضوًا [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) لتطبيق فلاتر متعددة ، وتسمح طريقة إضافة فئة `PostProcessings` بدمج فلتر قبل العرض.
###  **Pروغرامينغ ple وافرة**
يُطبق مثال الرمز هذا تأثير مرئي على عرض 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
