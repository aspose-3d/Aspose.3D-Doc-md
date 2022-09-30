---
title: متطلبات النظام
type: docs
weight: 50
url: /ar/python-net/system-requirements/
description: The متطلبات النظام ل Aspose.3D ل Python via .NET.
---
## **Oفيرفيو**
` `To بناء والتلاعب 3D تنسيقات الوثائق ، الجهاز الذي Aspose.3D ل Python via .NET يعمل على لا تحتاج إلى النمذجة وتقديم البرامج المثبتة. Aspose.3D ل Python via .NET API يتضمن أيضا محرك توليد الوثائق.
## **SupOperating Syالجذعية**
Aspose.3D ل Python via .NET يدعم أي 64 بت أو 32 بت نظام التشغيل حيث يتم تثبيت Python 3.5 أو في وقت لاحق.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Operating stem yالجذعية</td>
        <td style="font-weight: bold; width:400px">Erنصب</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003 Server (x64 ، x86)</li>
                <li>Windows 2008 Server (x64 ، x86)</li>
                <li>Windows 2012 Server (x64 ، x86)</li>
                <li>Windows 2012 R2 Server (x64 ، x86)</li>
                <li>Windows 2016 Server (x64 ، x86)</li>
                <li>Windows 2019 Server (x64 ، x86)</li>
                <li>Windows XP (x64 ، x86)</li>
                <li>Windows Vista (x64 ، x86)</li>
                <li>Windows 7 (x64 ، x86)</li>
                <li>Windows 8, 8.1 (x64, x86)</li>
                <li>Windows 10 (x64 ، x86)</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Linux</td>
        <td>
            <ul>
                <li>Uبونتو</li>
                <li>OpenSUE E</li>
                <li>CentOS</li>
                <li>وغيرها</li>
            </ul>
        </td>
    </tr>
</table>


## Equiyالجذعية equiequirements ل ararget Linux latlatform

- GCC-6 مكتبات وقت التشغيل (أو أحدث).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): قلم Oource ource تنفيذ GD07API.

- Cies من .NET ore خام unوقت الفراغ. Instيعادل .NET ore خام unغير الوقت نفسه هو NOT المطلوبة.

- Fأو Python 3.5-3.7: Tهو `pymalloc` بناء من Python هناك حاجة. The `--with-pymalloc` Python يتم تمكين خيار البناء بشكل افتراضي. بشكل غير عادي ، يتم وضع علامة على بناء `pymalloc` من Python مع لاحقة `m` في اسم الملف.

- `libpython` مكتبة مشتركة Python. The `--enable-shared` Python يتم تعطيل خيار البناء بشكل افتراضي ، وبعض التوزيعات Python لا تحتوي على المكتبة المشتركة `libpython`. Fأو بعض منصات لينكس ، يمكن تثبيت المكتبة المشتركة `libpython` باستخدام مدير الحزمة ، على سبيل المثال: `sudo apt-get install libpython3.7`. Tهو المشكلة الشائعة هي أن مكتبة `libpython` مثبتة في موقع مختلف عن موقع النظام القياسي للمكتبات المشتركة. Tيمكن إصلاح المشكلة باستخدام خيارات بناء Python لضبط مسارات المكتبة البديلة عند تجميع Python ، أو ثابتة عن طريق إنشاء رابط رمزي إلى ملف مكتبة `libpython` في موقع النظام القياسي للمكتبات المشتركة. بشكل غير عادي ، اسم ملف المكتبة المشتركة `libpython` هو `libpythonX.Ym.so.1.0` ل Python 3.5-3.7 ، أو `libpythonX.Y.so.1.0` ل Python 3.8 أو في وقت لاحق (على سبيل المثال: ليبيثون3.7m. so.1.0 ، ليبيثون3.9.so. 1.0).



Furthermore ، أي نظام تشغيل يمكن تثبيت Mono(.NET 4.0 Fدعم ramework) أو استخدام .NET core يمكن استخدام Aspose.3D ل Python via .NET.
## **Rإنديرينغ**
### **Vأولكان**
Aspose.3D ل Python via .NET يتطلب منصة Vulkan x64 ، لا يتم دعم x86.

- AMD adadeon 7700 سلسلة وأحدث
- NVIDIGeeForce 600 سلسلة وأحدث
- Iنتيل Sكيليك وأحدث
