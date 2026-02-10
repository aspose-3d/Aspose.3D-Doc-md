---
title: Work مع Xath ath-ike ايك ject حقن eries
type: docs
weight: 120
url: /ar/python-net/work-with-xpath-like-object-queries/
description: باستخدام Aspose.3D for Python via .NET ، يمكنك تحديد كائن واحد أو أكثر أسفل العقدة الحالية باستخدام تركيب استعلام يشبه XPath. بناء جملة الاستعلام مستوحى من XPath ، لذا فإن معظم المفاهيم والنحو متشابهتان ، بناء جملة الاستعلام متوافق مع عنوان URL بحيث سيتم استخدامه في الإصدار السحابي الخاص بنا في المستقبل.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.3 أو أكبر.

{{% /alert %}} 
##  **Work مع Xath ath-ike ايك ject حقن eries**
باستخدام Aspose.3D for Python via .NET ، يمكنك تحديد كائن واحد أو أكثر أسفل العقدة الحالية باستخدام تركيب استعلام يشبه XPath. بناء جملة الاستعلام مستوحى من XPath ، لذا فإن معظم المفاهيم والنحو متشابهتان ، بناء جملة الاستعلام متوافق مع عنوان URL بحيث سيتم استخدامه في الإصدار السحابي الخاص بنا في المستقبل. عادة ، يتكون بناء الجملة من**Pإعادة إصلاح ame ame onondition** / **Name onondition** /.

|**إعادة إصلاح P=**|**Esالاستبدال =**|
| :- | :- |
|//|Global محدد ، يتم التعامل مع أي سليل كعقدة الجذر لأداء التحديد|
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

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Camera, Light

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
# Create a scene for testing
s = Scene()
a = s.root_node.create_child_node("a")
a.create_child_node("a1")
a.create_child_node("a2")
s.root_node.create_child_node("b")
c = s.root_node.create_child_node("c")
c.create_child_node("c1").add_entity(Camera("cam"))
c.create_child_node("c2").add_entity(Light("light"))
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
# select objects that has type Camera or name is 'light' whatever it's located.
objects = s.root_node.select_objects("//*[(@Type = 'Camera') or (@Name = 'light')]")
# Select single camera object under the child nodes of node named 'c' under the root node
c1 = s.root_node.select_single_object("/c/*/<Camera>")
#  Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the
obj = s.root_node.select_single_object("a1")
# Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.
obj = s.root_node.select_single_object("/")

{{< /highlight >}}
