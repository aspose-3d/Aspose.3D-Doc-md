---
title: Aspose.3D for .NET 19.3 tes elease ootes
type: docs
weight: 100
url: /ar/net/aspose-3d-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.3](https://www.nuget.org/packages/Aspose.3D/19.3.0)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-471 |Xath مثل طرق معالجة الكائن|ميزة ew ew|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
#### **Aطريقة dded حدد ingleOحقن في الفئة com.aspose.threed. oode**
{{< highlight "java" >}}

 /// <summary>

/// Select single object under current node using XPath-like query syntax.

/// </summary>

/// <param name="path"></param>

/// <exception cref="ParseException">ParseException will be thrown if the path contains malformed query.</exception>

/// <returns></returns>

public Aspose.ThreeD.A3DObject SelectSingleObject(string path)

{{< /highlight >}}
#### **Aطريقة dded jecelectOالقاذفات في الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

 /// <summary>

/// Select multiple objects under current node using XPath-like query syntax.

/// </summary>

/// <param name="path"></param>

/// <exception cref="ParseException">ParseException will be thrown if the path contains malformed query.</exception>

/// <returns></returns>

public System.Collections.Generic.List<Aspose.ThreeD.A3DObject> SelectObjects(string path)

{{< /highlight >}}

Following هو رمز العينة للاستعلام عن كائن واحد أو أكثر:

{{< highlight "java" >}}

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

Assert.AreEqual(2, objects.Count);

Assert.IsInstanceOf<Camera>(objects[0]);

Assert.IsInstanceOf<Light>(objects[1]);

//Select single camera object under the child nodes of node named 'c' under the root node

var c1 = s.RootNode.SelectSingleObject("/c/*/<Camera>");

Assert.IsNotNull(c1);

// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the 

var obj = s.RootNode.SelectSingleObject("a1");

Assert.AreEqual("a1", obj.Name);

//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.

obj = s.RootNode.SelectSingleObject("/");

Assert.NotNull(obj);

Assert.IsInstanceOf<Node>(obj);

Assert.AreEqual(s.RootNode, obj);

{{< /highlight >}}

Tكان بناء الجملة الاستعلام مستوحاة من ath ath ath ، لذلك معظم المفاهيم وبناء الجملة متشابهة ، بناء الجملة الاستعلام متوافق مع Uath ath لذلك سيتم استخدامه في نسخة سحابة لدينا في المستقبل. Usually ، يتكون بناء الجملة من قبل**Pإعادة إصلاح ame ame onondition** / **Name onondition** /.

|**إعادة إصلاح P=**|**Esالاستبدال =**|
|:- |:- |
||Global محدد ، يتم التعامل مع أي سليل كعقدة الجذر لأداء التحديد|
|/|Root محدد ، يستخدم سلف واحد فقط للبحث عن|
|Oثر|Sssume إنه اسم ، وحدد الكائن بالاسم في وضع محدد عالمي|
Tانه اسم هو سلسلة التي تطابق اسم الكائن ، أو البدل '*' يستخدم لتتناسب مع أي اسم. Tهو شرط هو تعبير لتحديد ما إذا كان لتحديد الكائن ، ومشغلي منطقي (لا) و أو ، ومشغلي المقارنة>/</>=/<=/=/!= معتمدة. To ccccess خاصية في التعبير شرط ، يتم استخدام '@' بادئة ، على سبيل المثال @ Name سوف تقرأ خاصية ame ame. يتم دعم بناء جملة اختصار A لنوع الاختبار من قبل <Mesh> ، وهذا يعادل [@ ype ype = 'eshesh'] ، سيتم التعامل مع المعرفات دون اقتباس كسلسلة.
#### **Elect انتخاب جميع العقد باستخدام بناء الجملة العالمي محدد:**
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
#### **Elect اختيار عقدة المستوى الثاني مع الأم مرئية:**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}
