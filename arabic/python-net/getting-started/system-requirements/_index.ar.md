---
title: متطلبات النظام
type: docs
weight: 50
url: /ar/python-net/system-requirements/
description: متطلبات النظام مقابل Aspose.3D for Python via .NET.
---
##  **Oفيرفيو**
` ` لإنشاء تنسيقات مستندات 3D ومعالجتها ، لا تحتاج الماكينة التي يعمل بها Aspose.3D for Python via .NET إلى تثبيت برنامج النمذجة وتقديم. يشتمل Aspose.3D for Python via .NET API أيضًا على محرك توليد المستندات.
##  **SupOperating Syالجذعية**
يدعم Aspose.3D for Python via .NET أي نظام تشغيل 64 بت أو 32 بت حيث يتم تثبيت Python 3.5 أو الأحدث.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Operating stem yالجذعية</td>
        <td style="font-weight: bold; width:400px">Erنصب</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003 Server (x64, x86)</li>
                <li>Windows 2008 Server (x64, x86)</li>
                <li>Windows 2012 Server (x64, x86)</li>
                <li>خادم R2 Windows 2012 (x64, x86)</li>
                <li>خادم Windows 2016 (x64, x86)</li>
                <li>Windows 2019 Server (x64, x86)</li>
                <li>Windows XP (x64 ، x86)</li>
                <li>Windows فيستا (x64, x86)</li>
                <li>Windows 7 (x64, x86)</li>
                <li>Windows 8 ، 8.1 (x64 ، x86)</li>
                <li>Windows 10 (x64, x86)</li>
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
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): تطبيق مفتوح المصدر لـ GDI API.

- تبعيات وقت تشغيل أساسي بقيمة .NET. تثبيت .NET Core وقت التشغيل نفسه غير مطلوب.

- For Python 3.5-3.7: The `pymalloc` build of Python is needed. The `--with-pymalloc` Python build option is enabled by default. Typically, the `pymalloc` build of Python is marked with `m` suffix in the filename.

- شارك `libpython` مكتبة Python. تم تعطيل خيار إنشاء `--enable-shared` Python افتراضيًا ، ولا تحتوي بعض توزيعات Python على المكتبة المشتركة `libpython`. بالنسبة لبعض منصات لينكس ، يمكن تثبيت المكتبة المشتركة `libpython` باستخدام مدير الحزم ، على سبيل المثال: `sudo apt-get install libpython3.7`. المشكلة الشائعة هي أن مكتبة `libpython` مثبتة في موقع مختلف عن موقع النظام القياسي للمكتبات المشتركة. يمكن إصلاح المشكلة باستخدام خيارات الإنشاء Python لتعيين مسارات مكتبة بديلة عند تجميع Python ، أو إصلاحها بإنشاء ارتباط رمزي إلى ملف مكتبة `libpython` في الموقع القياسي للنظام للمكتبات المشتركة. عادةً ، يكون اسم ملف المكتبة المشترك `libpython` `libpythonX.Ym.so.1.0` لـ Python 3.5-3.7 ، أو `libpythonX.Y.so.1.0` لـ Python 3.8 أو الأحدث (على سبيل المثال: libpython3.7m.so.1.0, libpython3.9.so.1.0).



علاوة على ذلك ، يمكن لأي نظام تشغيل يمكنه تثبيت Mono(.NET 4.0 دعم الإطار) أو استخدام .NET core استخدام Aspose.3D for Python via .NET.
##  **Rإنديرينغ**
###  **Vأولكان**
Aspose.3D for Python via .NET requires Vulkan x64 platform, x86 is not supported.

- AMD adadeon 7700 سلسلة وأحدث
- NVIDIGeeForce 600 سلسلة وأحدث
- Iنتيل Sكيليك وأحدث
