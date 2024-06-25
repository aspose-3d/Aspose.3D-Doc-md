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

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.py" >}}
