---
title: Declaration
type: docs
weight: 30
url: /ar/net/declaration/
---
{{% alert color="primary" %}} 

بشكل عام ، تتطلب جميع مكونات Aspose .NET مجموعة أذونات الثقة الكاملة. السبب هو أن مكونات Aspose for .NET تحتاج إلى الوصول إلى إعدادات التسجيل وملفات النظام بخلاف الدليل الافتراضي لعمليات معينة مثل تحليل الخطوط وما إلى ذلك. علاوة على ذلك ، مكونات Aspose for .NET (بما في ذلك Aspose.3D for .NET) تستند إلى فئات النظام .NET الأساسية التي تتطلب أيضًا تعيين أذونات الثقة الكاملة في العديد من الحالات.

{{% /alert %}} 
##  **تحدي الثقة الجزئية/الثقة المتوسطة**
Internet Service Providers hosting multiple applications from different companies mostly enforce a Medium Trust security level. Moreover, sometimes you need to host multiple applications on a shared server, such as in an ISP or other scenarios, you have to use the Medium trust level to constrain the applications. The ASP.NET Medium trust level provides a constrained execution environment that is suitable for isolating multiple applications hosted on ISP servers. In case of .NET 2.0, such a security level may set the following constraints which could affect the ability of Aspose.3D for .NET to perform properly, for example:

- **إذن التسجيل غير متاح**. هذا يعني أنه لا يمكنك الوصول إلى السجل ، وهو أمر مطلوب لتعداد الخطوط المثبتة عند تقديم جداول البيانات أو المستندات الأخرى.
- **Fileopermission مقيدة**. هذا يعني أنه يمكنك فقط الوصول إلى الملفات في التسلسل الهرمي للدليل الافتراضي للتطبيق الخاص بك.
##  **استخدم Aspose.3D for .NET على مجموعة أذونات الثقة المتوسطة**
يمكنك اتباع بعض التوصيات لتشغيل Aspose.3D for .NET على مستوى الثقة المتوسط أو بيئة الخادم المشتركة:

- لتعيين ملف الترخيص في الكود الخاص بك ، من الأفضل استدعاء طريقة license. SetLicense(Stream) بدلاً من ذلك بعد الحصول على ملف الترخيص في الجداول.

راجع المثال التالي الذي يوضح كيفية استخدام/تشغيل Aspose.3D for .NET في وضع الثقة المتوسطة.

{{< highlight "csharp" >}}

 // Instantiate the License object

Aspose.ThreeD.License lic = new Aspose.ThreeD.License();

// Get the license file into stream

FileStream stream = new FileStream("Aspose._3D.lic", FileMode.Open);

// Set the License stream

lic.SetLicense(stream);

// Close the stream

stream.Close();

//Open the template file

Scene scene = new Scene("test.obj");

// Save the OBJ file

scene.Save("dest.obj", FileFormat.WavefrontOBJ);



{{< /highlight >}}





