---
title: Work with XPath-Like Object Queries
type: docs
weight: 120
url: /net/work-with-xpath-like-object-queries/
description: Using Aspose.3D for .NET, you can select one or more objects under the current node using XPath-Like query syntax. The query syntax was inspired by XPath, so most concepts and syntax are similar, the query syntax is compatible with URL so it will be used in our cloud version in the future. 
---

{{% alert color="primary" %}} 

This feature is supported by version 19.3 or greater.

{{% /alert %}} 
## **Work with XPath-Like Object Queries**
Using Aspose.3D for .NET, you can select one or more objects under the current node using XPath-Like query syntax. The query syntax was inspired by XPath, so most concepts and syntax are similar, the query syntax is compatible with URL so it will be used in our cloud version in the future. Usually, a syntax is composed by **Prefix Name Condition** / **Name Condition** /.

|**Prefix=**|**Description=**|
| :- | :- |
| // |Global selector, any descendant is treated as the root node to perform the selection |
|/|Root selector, only one ancestor is used to look up |
|Other |Assume it's a name, and select the object by name in global selector mode |
The name is a string that matches the object's name, or wildcard `*` is used to match any name. The condition is an expression to decide whether to select the object, boolean operators (not) and or, comparison operators `>/</>=/<=/=/!=` are supported. To Access a property in the condition expression, '@' prefix is used, e.g. `@Name` will read the Name property. A shortcut syntax for testing type is supported by `<Mesh>`, this is equivalent to `[@Type = 'Mesh']`, identifiers without a quote will be treated as a string.
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
