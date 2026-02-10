---
title: Arbeta med XPath- liknande objektförfrågningar
type: docs
weight: 60
url: /sv/java/work-with-xpath-like-object-queries/
description: Använder Aspose. 3D for Java, du kan välja ett eller flera objekt under nuvarande nod med XPath-liknande frågesyntax.
---
##  **Arbeta med XPath- liknande objektförfrågningar**
Använder Aspose. 3D for Java, du kan välja ett eller flera objekt under nuvarande nod med XPath-liknande frågesyntax. Söksyntaxen inspirerades av XPath, så de flesta koncept och syntax är liknande, sökningen syntax är kompatibel med URL så den kommer att användas i vår molnversion i framtiden. Vanligtvis består en syntax av en syntax**Prefixnamn villkor** / **Namnvillkor** /.

|**Prefix**|**Beskrivning**|
| :- | :- |
| // |Global väljare, varje ättling behandlas som rotnod för att utföra markeringen|
|/|Rotväljare, bara en förfader används för att söka upp.|
|Andra slag|Anta att det är ett namn, och välj objektet efter namn i globalt valläge|

Namnet är en sträng som matchar objektets namn, eller wildcard `*` används för att matcha vilket namn som helst. Villkoret är ett uttryck för att avgöra om att välja objektet, boolean operatörer (inte) och, jämförelseoperatörer `>/</>=/<=/=/!=` stöds. För att komma åt en egenskap i tillståndsuttrycket används '@' prefix, e. g. `@Name` läser egenskapen Namn. En genvägssyntax för testtyp stöds av `<Mesh>`, vilket motsvarar `[@Type = 'Mesh']`, Identifier utan citat kommer att behandlas som en sträng.
###  **Välj alla noder med hjälp av global syntaxväljare**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

Det här är den korta syntaxen av:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

Eller

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
###  **Välj en andra nivånod med en synlig överliggande**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}



Följande är provkoden för att fråga ett eller flera objekt:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
//Create a scene for testing
Scene s = new Scene();
// Create a child node
Node a = s.getRootNode().createChildNode("a");
// Create a sub-child node
a.createChildNode("a1");
// Create a sub-child node
a.createChildNode("a2");
// Create a child node
s.getRootNode().createChildNode("b");
// Create a child node
Node c = s.getRootNode().createChildNode("c");
// Create a sub-child node
c.createChildNode("c1").addEntity(new Camera("cam"));
// Create a sub-child node
c.createChildNode("c2").addEntity(new Light("light"));
/*
The hierarchy of the scene looks like:
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
List<A3DObject> objects = s.getRootNode().selectObjects("//*[(@Type = 'Camera') or (@Name = 'light')]");

//Select single camera object under the child nodes of node named 'c' under the root node
A3DObject c1 = s.getRootNode().selectSingleObject("/c/*/<Camera>");

// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the
A3DObject obj = s.getRootNode().selectSingleObject("a1");

//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.
obj = s.getRootNode().selectSingleObject("/");

{{< /highlight >}}
