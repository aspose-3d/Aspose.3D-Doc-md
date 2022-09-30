---
title: Aspose.3D for Java 19.3 tes elease ootes
type: docs
weight: 100
url: /ar/java/aspose-3d-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for Java 19.3](https://repository.aspose.com/repo/com/aspose/aspose-xps/19.3/).

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-471 |Xath مثل طرق معالجة الكائن|ميزة ew ew|

## **Public API و ackأكواردز hangمتوافق مع hangمعلقة**

See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for Java. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).

**Aطريقة dded حدد ingleOحقن في الفئة com.aspose.threed. oode**

{{< highlight "java" >}}

 /**

 * Select single object under current node using XPath-like query syntax.

 * @param path 

 * @throws ParseException ParseException will be thrown if the path contains malformed query.

 */

public A3DObject selectSingleObject(String path)

    throws ParseException;

{{< /highlight >}}

**Aطريقة dded حدد القاذفات في الفئة com.aspose.threed. oode**

{{< highlight "java" >}}

 /**

 * Select multiple objects under current node using XPath-like query syntax.

 * @param path 

 * @throws ParseException ParseException will be thrown if the path contains malformed query.

 */

public ArrayList<A3DObject> selectObjects(String path)

    throws ParseException;

{{< /highlight >}}

Following هو رمز العينة للاستعلام عن كائن واحد أو أكثر:

{{< highlight "java" >}}

 Scene s = new Scene();

Node a = s.getRootNode().createChildNode("a");

a.createChildNode("a1");

a.createChildNode("a2");

s.getRootNode().createChildNode("b");

Node c = s.getRootNode().createChildNode("c");

c.createChildNode("c1").addEntity(new Camera("cam"));

c.createChildNode("c2").addEntity(new Light("light"));

/*

The hierarchy of the scene looks like:

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

List<A3DObject> objects = s.getRootNode().selectObjects("//*[(@Type = 'Camera') or (@Name = 'light')]");

Assert.assertEquals(2, objects.size());

Assert.assertTrue(objects.get(0) instanceof Camera);

Assert.assertTrue(objects.get(1) instanceof Light);

//Select single camera object under the child nodes of node named 'c' under the root node

A3DObject c1 = s.getRootNode().selectSingleObject("/c/*/<Camera>");

Assert.assertNotNull(c1);

// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the

A3DObject obj = s.getRootNode().selectSingleObject("a1");

Assert.assertEquals("a1", obj.getName());

//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.

obj = s.getRootNode().selectSingleObject("/");

Assert.assertNotNull(obj);

Assert.assertTrue(obj instanceof Node);

Assert.assertEquals(s.getRootNode(), obj);

{{< /highlight >}}

Tكان بناء الجملة الاستعلام مستوحاة من ath ath ath ، لذلك معظم المفاهيم وبناء الجملة متشابهة ، بناء الجملة الاستعلام متوافق مع Uath ath لذلك سيتم استخدامه في نسخة سحابة لدينا في المستقبل. Usually ، يتكون بناء الجملة من قبل**Pإعادة إصلاح ame ame onondition** / **Name onondition** /.

|**إعادة إصلاح P=**|**Esالاستبدال =**|
|:- |:- |
||Global محدد ، يتم التعامل مع أي سليل كعقدة الجذر لأداء التحديد|
|/|Root محدد ، يستخدم سلف واحد فقط للبحث عن|
|Oثر|Sssume إنه اسم ، وحدد الكائن بالاسم في وضع محدد عالمي|
Tانه اسم هو سلسلة التي تطابق اسم الكائن ، أو البدل '*' يستخدم لتتناسب مع أي اسم. Tهو شرط هو تعبير لتحديد ما إذا كان لتحديد الكائن ، ومشغلي منطقي (لا) و أو ، ومشغلي المقارنة>/</>=/<=/=/!= معتمدة. To ccccess خاصية في التعبير شرط ، يتم استخدام '@' بادئة ، على سبيل المثال @ Name سوف تقرأ خاصية ame ame. يتم دعم بناء جملة اختصار A لنوع الاختبار من قبل <Mesh> ، وهذا يعادل [@ ype ype = 'eshesh'] ، سيتم التعامل مع المعرفات دون اقتباس كسلسلة.

**Elect انتخاب جميع العقد باستخدام بناء الجملة العالمي محدد:**

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

 **Elect اختيار عقدة المستوى الثاني مع الأم مرئية:**

 {{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}
