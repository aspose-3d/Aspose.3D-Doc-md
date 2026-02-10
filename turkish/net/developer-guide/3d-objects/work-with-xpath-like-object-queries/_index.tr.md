---
title: Xork ile Xath ath-Like Object eries ueries
type: docs
weight: 120
url: /tr/net/work-with-xpath-like-object-queries/
description: Using Aspose.3D for .NET, you can select one or more objects under the current node using XPath-Like query syntax. The query syntax was inspired by XPath, so most concepts and syntax are similar, the query syntax is compatible with URL so it will be used in our cloud version in the future. 
---
{{% alert color="primary" %}} 

This özelliği 19.3 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
##  **Xork ile Xath ath-Like Object eries ueries**
Using Aspose.3D for .NET, you can select one or more objects under the current node using XPath-Like query syntax. The query syntax was inspired by XPath, so most concepts and syntax are similar, the query syntax is compatible with URL so it will be used in our cloud version in the future. Usually, a syntax is composed by **Prefix dition ame dition ondition** / **Name dition ondition** /.

|**Prefix =**|**Description =**|
| :- | :- |
| // |Global seçici, herhangi bir descendant seçimi gerçekleştirmek için kök düğüm olarak tedavi edilir|
|/|Root seçici, sadece bir atası bakmak için kullanılır|
|Other|Assume bir isim ve nesneyi küresel seçici modunda isme göre seçin|
İsim, nesnenin adıyla eşleşen bir dizedir veya herhangi bir isimle eşleştirmek için wildcard `*` kullanılır. Durum, nesneyi, boole operatörlerini (değil) ve karşılaştırma operatörlerinin `>/</>=/<=/=/!=` desteklenip desteklenmeyeceğine karar vermek için bir ifadedir. Durum ifadesindeki bir mülke erişmek için, '@' öneki kullanılır, e.g. `@Name` ad özelliğini okuyacak. Test türü için bir kısayol sözdizimi `<Mesh>` tarafından desteklenir, bu `[@Type = 'Mesh']` eşdeğerdir, bir teklif olmadan tanımlayıcılar bir dize olarak ele alınacaktır.
###  **Ssözdizimi küresel seçici kullanarak tüm düğümleri seçin**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

This kısa sözdizimidir:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

Veya

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
###  **Sgörünür bir ebeveyn ile ikinci seviye bir düğüm seç**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

Following bir veya daha fazla nesneyi sorgulamak için örnek koddur:

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
