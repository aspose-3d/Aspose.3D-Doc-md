---
title: 使用类似XPath的对象查询
type: docs
weight: 120
url: /zh/net/work-with-xpath-like-object-queries/
description: 使用 Aspose.3D for .NET，可以使用类似XPath的查询语法选择当前节点下的一个或多个对象。查询语法受到XPath的启发，因此大多数概念和语法都是相似的，查询语法与URL兼容，因此将来将在我们的云版本中使用。
---
{{% alert color="primary" %}} 

19.3或更高版本支持此功能。

{{% /alert %}} 
##  **使用类似XPath的对象查询**
使用 Aspose.3D for .NET，可以使用类似XPath的查询语法选择当前节点下的一个或多个对象。查询语法受到XPath的启发，因此大多数概念和语法都是相似的，查询语法与URL兼容，因此将来将在我们的云版本中使用。通常，语法由**前缀名称条件** / **名称条件** /.

|**前缀 =**|**描述 =**|
| :- | :- |
| // |全局选择器，任何后代都被视为根节点来执行选择|
|/|根选择器，只使用一个祖先来查找|
|其他|假设它是一个名称，并在全局选择器模式下按名称选择对象|
名称是与对象名称匹配的字符串，或使用通配符 `*` 匹配任何名称。条件是决定是否选择对象的表达式，支持布尔运算符 (not) 和or，比较运算符 `>/</>=/<=/=/!=`。要访问条件表达式中的属性，使用 “@” 前缀，例如 `@Name` 将读取Name属性。`<Mesh>` 支持测试类型的快捷语法，这相当于 `[@Type = 'Mesh']`，没有引号的标识符将被视为字符串。
###  **使用语法全局选择器选择所有节点**
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
###  **选择具有可见父级的第二级节点**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

以下是查询一个或多个对象的示例代码:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.cs" >}}
