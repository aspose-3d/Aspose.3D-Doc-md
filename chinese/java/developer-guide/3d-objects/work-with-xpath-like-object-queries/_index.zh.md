---
title: 使用类似XPath的对象查询
type: docs
weight: 60
url: /zh/java/work-with-xpath-like-object-queries/
description: 使用Aspose.3D for Java，可以使用类似XPath的查询语法在当前节点下选择一个或多个对象。
---
## **使用类似XPath的对象查询**
使用Aspose.3D for Java，可以使用类似XPath的查询语法在当前节点下选择一个或多个对象。查询语法的灵感来自XPath，因此大多数概念和语法都是相似的，查询语法与URL兼容，因此将来将在我们的云版本中使用。通常，语法是由**前缀名称条件** / **名称条件** /.

|**前缀**|**描述**|
|:- |:- |
|// |全局选择器，任何后代都被视为根节点来执行选择|
|/|根选择器，只使用一个祖先来查找|
|其他|假设它是一个名称，并在全局选择器模式下按名称选择对象|

名称是与对象名称匹配的字符串，或者通配符`*`用于匹配任何名称。条件是用于决定是否选择对象的表达式，支持布尔运算符 (不) 和或比较运算符`>/</>=/<=/=/!=`。要访问条件表达式中的属性，使用 “@” 前缀，例如`@Name`将读取Name属性。`<Mesh>`支持用于测试类型的快捷语法，这等效于`[@Type = 'Mesh']`，不带引号的标识符将被视为字符串。
### **使用语法全局选择器选择所有节点**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

这是的简短语法:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

或者

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
### **选择具有可见父级的第二级节点**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}



以下是查询一个或多个对象的示例代码:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-objects-XPathLikeObjectQueries-XPathLikeObjectQueries.java" >}}
