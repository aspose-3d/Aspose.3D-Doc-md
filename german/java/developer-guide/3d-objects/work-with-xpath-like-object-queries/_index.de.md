---
title: Arbeiten Sie mit XPath-ähnlichen Objekt abfragen
type: docs
weight: 60
url: /de/java/work-with-xpath-like-object-queries/
description: Mit Aspose.3D for Java können Sie ein oder mehrere Objekte unter dem aktuellen Knoten mithilfe der XPath-Like-Abfrage syntax auswählen.
---
##  **Arbeiten Sie mit XPath-ähnlichen Objekt abfragen**
Mit Aspose.3D for Java können Sie ein oder mehrere Objekte unter dem aktuellen Knoten mithilfe der XPath-Like-Abfrage syntax auswählen. Die Abfrage syntax wurde von XPath inspiriert, sodass die meisten Konzepte und Syntax ähnlich sind. Die Abfrage syntax ist mit URL kompatibel, sodass sie in Zukunft in unserer Cloud-Version verwendet wird. Normaler weise besteht eine Syntax aus**Präfix Name Bedingung** / **Name Bedingung** /.

|**Präfix**|**Beschreibung**|
| :- | :- |
| // |Globaler Selektor, jeder Nachkomme wird als Stamm knoten behandelt, um die Auswahl durch zuführen|
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
