+++
title = "Work with XPath-Like Object Queries" 
description = "" 
weight = 12050 
+++

Aspose.3D for .NET : Work with XPath-Like Object Queries  

# Aspose.3D for .NET : Work with XPath-Like Object Queries


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Work with XPath-Like Object Queries ](#WorkwithXPath-LikeObjectQueries-WorkwithXPath-LikeObjectQueries)
    *   1.1 [Select all nodes using syntax global selector](#WorkwithXPath-LikeObjectQueries-Selectallnodesusingsyntaxglobalselector)
    *   1.2 [Select a second level node with a visible parent](#WorkwithXPath-LikeObjectQueries-Selectasecondlevelnodewithavisibleparent)
{{< /panel >}}
 

 

This feature is supported by version 19.3 or greater.

## Work with XPath-Like Object Queries 

Using Aspose.3D for .NET, you can select one or more objects under the current node using XPath-Like query syntax. The query syntax was inspired by XPath, so most concepts and syntax are similar, the query syntax is compatible with URL so it will be used in our cloud version in the future. Usually, a syntax is composed by**Prefix Name Condition** / **Name Condition** /.

{{< table style="table-striped" >}}
|Prefix=|Description=|
|:----|:----|
| |Global selector, any descendant is treated as the root node to perform the selection |
|/|Root selector, only one ancestor is used to look up |
|Other |Assume it's a name, and select the object by name in global selector mode |
{{< /table >}}

The name is a string that matches the object's name, or wildcard '\*' is used to match any name. The condition is an expression to decide whether to select the object, boolean operators (not) and or, comparison operators >/</>=/<=/=/!= are supported. To Access a property in the condition expression, '@' prefix is used, e.g. @Name will read the Name property. A shortcut syntax for testing type is supported by <Mesh>, this is equivalent to \[@Type = 'Mesh'\], identifiers without a quote will be treated as a string.

### Select all nodes using syntax global selector

{{< code lang="cs" >}}
//<Node>
{{< /code >}}

This is the short syntax of:

{{< code lang="cs" >}}
//\*\[<Node>\]
{{< /code >}}

or

{{< code lang="cs" >}}
//\*\[@Type = Node\]
{{< /code >}}

### Select a second level node with a visible parent

{{< code lang="cs" >}}
//<Node>\[@Visible\]/<Node>
{{< /code >}}

  

Following is the sample code to query one or more objects:

