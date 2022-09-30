---
title: Work مع Xath ath-ike ايك ject حقن eries
type: docs
weight: 60
url: /ar/java/work-with-xpath-like-object-queries/
description: Using Aspose.3D for Java ، يمكنك اختيار واحد أو أكثر من الكائنات تحت العقدة الحالية باستخدام synath ath-ike إيكي الاستعلام بناء الجملة.
---
## **Work مع Xath ath-ike ايك ject حقن eries**
Using Aspose.3D for Java ، يمكنك اختيار واحد أو أكثر من الكائنات تحت العقدة الحالية باستخدام synath ath-ike إيكي الاستعلام بناء الجملة. Tكان بناء الجملة الاستعلام مستوحاة من ath ath ath ، لذلك معظم المفاهيم وبناء الجملة متشابهة ، بناء الجملة الاستعلام متوافق مع Uath ath لذلك سيتم استخدامه في نسخة سحابة لدينا في المستقبل. Usually ، يتكون بناء الجملة من قبل**Pإعادة إصلاح ame ame onondition** / **Name onondition** /.

|**إعادة إصلاح P**|**نقل D**|
|:- |:- |
|// |Global محدد ، يتم التعامل مع أي سليل كعقدة الجذر لأداء التحديد|
|/|Root محدد ، يستخدم سلف واحد فقط للبحث عن|
|Oثر|Sssume إنه اسم ، وحدد الكائن بالاسم في وضع محدد عالمي|

Tهو الاسم عبارة عن سلسلة تتطابق مع اسم الكائن ، أو يستخدم بطاقة البدل `*` لتتناسب مع أي اسم. Tانه شرط هو تعبير عن أن تقرر ما إذا كان لتحديد الكائن ، ومشغلي منطقي (لا) و أو ، يتم دعم مشغلي المقارنة `>/</>=/<=/=/!=`. To ccccess خاصية في التعبير الشرط ، يتم استخدام '@' prefix ، على سبيل المثال `@Name` سوف يقرأ خاصية ame ame. يتم دعم بناء جملة اختصار A لنوع الاختبار من قبل `<Mesh>` ، وهذا يعادل `[@Type = 'Mesh']` ، سيتم التعامل مع المعرفات دون اقتباس كسلسلة.
### **Elect انتخاب جميع العقد باستخدام بناء الجملة العالمي محدد**
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
### **Elect اختيار عقدة المستوى الثاني مع الأم مرئية**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}



Following هو رمز العينة للاستعلام عن كائن واحد أو أكثر:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-objects-XPathLikeObjectQueries-XPathLikeObjectQueries.java" >}}
