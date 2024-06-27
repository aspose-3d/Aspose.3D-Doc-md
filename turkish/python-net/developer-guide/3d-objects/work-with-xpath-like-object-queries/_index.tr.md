---
title: Xork ile Xath ath-Like Object eries ueries
type: docs
weight: 120
url: /tr/python-net/work-with-xpath-like-object-queries/
description: Aspose.3D for Python via .NET kullanarak, xpath benzeri sorgu sözdizimini kullanarak mevcut düğüm altında bir veya daha fazla nesne seçebilirsiniz. Sorgu sözdizimi xway'den ilham aldı, bu yüzden çoğu kavram ve sözdizimi benzer, sorgu sözdizimi url ile uyumludur, bu yüzden gelecekte bulut sürümümüzde kullanılacaktır.
---
{{% alert color="primary" %}} 

This özelliği 19.3 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
##  **Xork ile Xath ath-Like Object eries ueries**
Aspose.3D for Python via .NET kullanarak, xpath benzeri sorgu sözdizimini kullanarak mevcut düğüm altında bir veya daha fazla nesne seçebilirsiniz. Sorgu sözdizimi xway'den ilham aldı, bu yüzden çoğu kavram ve sözdizimi benzer, sorgu sözdizimi url ile uyumludur, bu yüzden gelecekte bulut sürümümüzde kullanılacaktır. Genellikle bir sözdizimi oluşur**Prefix dition ame dition ondition** / **Name dition ondition** /.

|**Prefix =**|**Description =**|
| :- | :- |
|//|Global seçici, herhangi bir descendant seçimi gerçekleştirmek için kök düğüm olarak tedavi edilir|
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

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.py" >}}
