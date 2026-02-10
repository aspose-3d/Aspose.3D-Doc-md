---
title: Work مع Xath ath-ike ايك ject حقن eries
type: docs
weight: 120
url: /ar/net/work-with-xpath-like-object-queries/
description: باستخدام Aspose.3D for .NET ، يمكنك تحديد كائن واحد أو أكثر أسفل العقدة الحالية باستخدام بناء استعلام يشبه XPath. بناء جملة الاستعلام مستوحى من XPath ، لذا فإن معظم المفاهيم والنحو متشابهتان ، بناء جملة الاستعلام متوافق مع عنوان URL بحيث سيتم استخدامه في الإصدار السحابي الخاص بنا في المستقبل.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.3 أو أكبر.

{{% /alert %}} 
##  **Work مع Xath ath-ike ايك ject حقن eries**
باستخدام Aspose.3D for .NET ، يمكنك تحديد كائن واحد أو أكثر أسفل العقدة الحالية باستخدام بناء استعلام يشبه XPath. بناء جملة الاستعلام مستوحى من XPath ، لذا فإن معظم المفاهيم والنحو متشابهتان ، بناء جملة الاستعلام متوافق مع عنوان URL بحيث سيتم استخدامه في الإصدار السحابي الخاص بنا في المستقبل. عادة ، يتكون بناء الجملة من**Pإعادة إصلاح ame ame onondition** / **Name onondition** /.

|**إعادة إصلاح P=**|**Esالاستبدال =**|
| :- | :- |
| // |Global محدد ، يتم التعامل مع أي سليل كعقدة الجذر لأداء التحديد|
|/|Root محدد ، يستخدم سلف واحد فقط للبحث عن|
|Oثر|Sssume إنه اسم ، وحدد الكائن بالاسم في وضع محدد عالمي|
الاسم عبارة عن سلسلة تتطابق مع اسم الكائن ، أو يتم استخدام wildcard `*` لمطابقة أي اسم. الشرط عبارة عن تعبير لتحديد ما إذا كان سيتم تحديد الكائن ، أو المشغلات المنطقية (غير) أو مشغلات المقارنة `>/</>=/<=/=/!=` مدعومة. للوصول إلى خاصية في تعبير الشرط ، تم استخدام بادئة "@" ، على سبيل المثال ، سيقرأ `@Name` خاصية الاسم. بناء جملة مختصر لنوع الاختبار مدعوم بـ `<Mesh>` ، وهذا يعادل `[@Type = 'Mesh']` ، وستعامل المعرّفات التي لا تحمل عرض أسعار كسلسلة.
###  **Elect انتخاب جميع العقد باستخدام بناء الجملة العالمي محدد**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

Tله هو بناء الجملة قصيرة من:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

أو

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
###  **Elect اختيار عقدة المستوى الثاني مع الأم مرئية**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

Following هو رمز العينة للاستعلام عن كائن واحد أو أكثر:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
//Create a scene for testing 
Scene s = new Scene();
var a = s.RootNode.CreateChildNode("a");
a.CreateChildNode("a1");
a.CreateChildNode("a2");
s.RootNode.CreateChildNode("b");
var c = s.RootNode.CreateChildNode("c");
c.CreateChildNode("c1").AddEntity(new Camera("cam"));
c.CreateChildNode("c2").AddEntity(new Light("light"));
/*The hierarchy of the scene looks like:
 - Root
    - a
        - a1
        - a2
    - b
    - c
        - c1
            - cam
        - c2
            - light
             */
//select objects that has type Camera or name is 'light' whatever it's located.
var objects = s.RootNode.SelectObjects("//*[(@Type = 'Camera') or (@Name = 'light')]");
//Select single camera object under the child nodes of node named 'c' under the root node
var c1 = s.RootNode.SelectSingleObject("/c/*/<Camera>");
// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the 
var obj = s.RootNode.SelectSingleObject("a1");
//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.
obj = s.RootNode.SelectSingleObject("/");

{{< /highlight >}}
