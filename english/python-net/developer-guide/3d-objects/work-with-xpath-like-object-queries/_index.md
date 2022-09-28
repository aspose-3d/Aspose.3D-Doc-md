---
title: Work with XPath-Like Object Queries
type: docs
weight: 120
url: /python-net/work-with-xpath-like-object-queries/
description: Using Aspose.3D for Python via .NET, you can select one or more objects under the current node using XPath-Like query syntax. The query syntax was inspired by XPath, so most concepts and syntax are similar, the query syntax is compatible with URL so it will be used in our cloud version in the future. 
---

{{% alert color="primary" %}} 

This feature is supported by version 19.3 or greater.

{{% /alert %}} 
## **Work with XPath-Like Object Queries**
Using Aspose.3D for Python via .NET, you can select one or more objects under the current node using XPath-Like query syntax. The query syntax was inspired by XPath, so most concepts and syntax are similar, the query syntax is compatible with URL so it will be used in our cloud version in the future. Usually, a syntax is composed by **Prefix Name Condition** / **Name Condition** /.

|**Prefix=**|**Description=**|
| :- | :- |
| |Global selector, any descendant is treated as the root node to perform the selection |
|/|Root selector, only one ancestor is used to look up |
|Other |Assume it's a name, and select the object by name in global selector mode |
The name is a string that matches the object's name, or wildcard '*' is used to match any name. The condition is an expression to decide whether to select the object, boolean operators (not) and or, comparison operators >/</>=/<=/=/!= are supported. To Access a property in the condition expression, '@' prefix is used, e.g. @Name will read the Name property. A shortcut syntax for testing type is supported by <Mesh>, this is equivalent to [@Type = 'Mesh'], identifiers without a quote will be treated as a string.
### **Select all nodes using syntax global selector**
{{< highlight java >}}

 //<Node>

{{< /highlight >}}

This is the short syntax of:

{{< highlight java >}}

 //*[<Node>]

{{< /highlight >}}

or

{{< highlight java >}}

 //*[@Type = Node]

{{< /highlight >}}
### **Select a second level node with a visible parent**
{{< highlight java >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

Following is the sample code to query one or more objects:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.py" >}}
