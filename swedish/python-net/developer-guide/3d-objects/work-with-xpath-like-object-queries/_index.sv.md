---
title: Arbeta med XPath- liknande objektförfrågningar
type: docs
weight: 120
url: /sv/python-net/work-with-xpath-like-object-queries/
description: Med Aspose.3D for Python via .NET kan du välja ett eller flera objekt under nuvarande nod med XPath-Liknande frågesyntax. Söksyntaxen inspirerades av XPath, så de flesta koncept och syntax är liknande, sökningen syntax är kompatibel med URL så den kommer att användas i vår molnversion i framtiden.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.3 eller större.

{{% /alert %}} 
##  **Arbeta med XPath- liknande objektförfrågningar**
Med Aspose.3D for Python via .NET kan du välja ett eller flera objekt under nuvarande nod med XPath-Liknande frågesyntax. Söksyntaxen inspirerades av XPath, så de flesta koncept och syntax är liknande, sökningen syntax är kompatibel med URL så den kommer att användas i vår molnversion i framtiden. Vanligtvis består en syntax av en syntax**Prefixnamn villkor** / **Namnvillkor** /.

|**Prefix=**|**Beskrivning=**|
| :- | :- |
|//|Global väljare, varje ättling behandlas som rotnod för att utföra markeringen|
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
