---
title: Xork ile Xath ath-Like Object eries ueries
type: docs
weight: 60
url: /tr/java/work-with-xpath-like-object-queries/
description: Using Aspose.3D for Java, mevcut düğümün altında bir veya daha fazla nesneyi Xath ath-ike ike sorgu sözdizimini kullanarak seçebilirsiniz.
---
## **Xork ile Xath ath-Like Object eries ueries**
Using Aspose.3D for Java, mevcut düğümün altında bir veya daha fazla nesneyi Xath ath-ike ike sorgu sözdizimini kullanarak seçebilirsiniz. To sorgu sözdizimi Xath ath tarafından ilham alındı, bu yüzden çoğu kavram ve sözdizimi benzer, sorgu sözdizimi Ucloud L ile uyumludur, bu yüzden gelecekte bulut sürümümüzde kullanılacaktır. Sually sually, bir sözdizimi oluşur**Prefix dition ame dition ondition** / **Name dition ondition** /.

|**Prefix**|**Description**|
|:- |:- |
|// |Global seçici, herhangi bir descendant seçimi gerçekleştirmek için kök düğüm olarak tedavi edilir|
|/|Root seçici, sadece bir atası bakmak için kullanılır|
|Other|Assume bir isim ve nesneyi küresel seçici modunda isme göre seçin|

The adı, nesnenin adıyla eşleşen bir dizedir veya herhangi bir isimle eşleştirmek için wildcard `*` kullanılır. The durumu, nesneyi, boole operatörlerini (değil) ve karşılaştırma operatörlerini `>/</>=/<=/=/!=` destekleyip desteklemeyeceğine karar vermek için bir ifadedir. Condition o condition c. koşul ifadesinde bir özellik, '@' önek kullanılır, örneğin `@Name` Name özelliğini okuyacak. A test türü için kısayol sözdizimi `<Mesh>` tarafından desteklenmektedir, bu 076481 481 eşdeğerdir, bir teklif olmadan tanımlayıcılar bir dize olarak ele alınacaktır.
### **Ssözdizimi küresel seçici kullanarak tüm düğümleri seçin**
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
### **Sgörünür bir ebeveyn ile ikinci seviye bir düğüm seç**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}



Following bir veya daha fazla nesneyi sorgulamak için örnek koddur:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-objects-XPathLikeObjectQueries-XPathLikeObjectQueries.java" >}}
