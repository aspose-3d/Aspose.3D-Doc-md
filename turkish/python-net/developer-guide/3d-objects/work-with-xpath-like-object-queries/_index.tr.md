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
