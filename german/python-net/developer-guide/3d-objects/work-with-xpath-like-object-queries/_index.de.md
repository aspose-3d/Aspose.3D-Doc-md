---
title: Arbeiten Sie mit XPath-ähnlichen Objekt abfragen
type: docs
weight: 120
url: /de/python-net/work-with-xpath-like-object-queries/
description: Mit Aspose.3D for Python via .NET können Sie ein oder mehrere Objekte unter dem aktuellen Knoten mithilfe der XPath-Like-Abfrage syntax auswählen. Die Abfrage syntax wurde von XPath inspiriert, sodass die meisten Konzepte und Syntax ähnlich sind. Die Abfrage syntax ist mit URL kompatibel, sodass sie in Zukunft in unserer Cloud-Version verwendet wird.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.3 oder höher unterstützt.

{{% /alert %}} 
##  **Arbeiten Sie mit XPath-ähnlichen Objekt abfragen**
Mit Aspose.3D for Python via .NET können Sie ein oder mehrere Objekte unter dem aktuellen Knoten mithilfe der XPath-Like-Abfrage syntax auswählen. Die Abfrage syntax wurde von XPath inspiriert, sodass die meisten Konzepte und Syntax ähnlich sind. Die Abfrage syntax ist mit URL kompatibel, sodass sie in Zukunft in unserer Cloud-Version verwendet wird. Normaler weise besteht eine Syntax aus**Präfix Name Bedingung** / **Name Bedingung** /.

|**Präfix =**|**Beschreibung =**|
| :- | :- |
|//|Globaler Selektor, jeder Nachkomme wird als Stamm knoten behandelt, um die Auswahl durch zuführen|
|/|Wurzel selektor, nur ein Vorfahr wird zum Nachschauen verwendet|
|Sonstige|Angenommen, es ist ein Name, und wählen Sie das Objekt nach Namen im globalen Auswahl modus aus|
Der Name ist eine Zeichenfolge, die mit dem Namen des Objekts überein stimmt, oder Platzhalter `*` wird verwendet, um mit einem beliebigen Namen überein zustimmen. Die Bedingung ist ein Ausdruck, um zu entscheiden, ob das Objekt ausgewählt werden soll. Boolesche Operatoren (nicht) und Vergleichs operatoren `>/</>=/<=/=/!=` werden unterstützt. Um auf eine Eigenschaft im Bedingung ausdruck zuzugreifen, wird das Präfix '@' verwendet, z. B. wird `@Name` die Eigenschaft Name lesen. Eine Verknüpfung syntax für den Testtyp wird von `<Mesh>` unterstützt. Dies entspricht `[@Type = 'Mesh']`. Bezeichner ohne Angebot werden als Zeichenfolge behandelt.
###  **Wählen Sie alle Knoten mithilfe des globalen Syntax-Selektors aus**
{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

Dies ist die kurze Syntax von:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

Oder

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}
###  **Wählen Sie einen Knoten der zweiten Ebene mit einem sichtbaren Elternteil aus**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

Es folgt der Beispielcode, um ein oder mehrere Objekte abzufragen:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.py" >}}
