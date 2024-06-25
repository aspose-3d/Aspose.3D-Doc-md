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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.cs" >}}
