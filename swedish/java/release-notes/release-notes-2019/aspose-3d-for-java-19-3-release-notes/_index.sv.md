---
title: Aspose.3D for Java 19,3 Utgivning
type: docs
weight: 100
url: /sv/java/aspose-3d-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 19,3](https://repository.aspose.com/repo/com/aspose/aspose-xps/19.3/).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-471 |XPath- liknande objekt adresseringsmetoder|Ny funktion|

## **Offentlig API och bakåts oförenliga förändringar**

Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

**Tillagd metod väljSingleObject i klass com.aspose.3reed.Node.**

{{< highlight "java" >}}

 /**

 * Select single object under current node using XPath-like query syntax.

 * @param path 

 * @throws ParseException ParseException will be thrown if the path contains malformed query.

 */

public A3DObject selectSingleObject(String path)

    throws ParseException;

{{< /highlight >}}

**Tillagd metod väljObjekt i klass com.aspose.3reed.Node.**

{{< highlight "java" >}}

 /**

 * Select multiple objects under current node using XPath-like query syntax.

 * @param path 

 * @throws ParseException ParseException will be thrown if the path contains malformed query.

 */

public ArrayList<A3DObject> selectObjects(String path)

    throws ParseException;

{{< /highlight >}}

Följande är provkoden för att fråga ett eller flera objekt:

{{< highlight "java" >}}

 Scene s = new Scene();

Node a = s.getRootNode().createChildNode("a");

a.createChildNode("a1");

a.createChildNode("a2");

s.getRootNode().createChildNode("b");

Node c = s.getRootNode().createChildNode("c");

c.createChildNode("c1").addEntity(new Camera("cam"));

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

Assert.assertEquals(2, objects.size());

Assert.assertTrue(objects.get(0) instanceof Camera);

Assert.assertTrue(objects.get(1) instanceof Light);

//Select single camera object under the child nodes of node named 'c' under the root node

A3DObject c1 = s.getRootNode().selectSingleObject("/c/*/<Camera>");

Assert.assertNotNull(c1);

// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the

A3DObject obj = s.getRootNode().selectSingleObject("a1");

Assert.assertEquals("a1", obj.getName());

//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.

obj = s.getRootNode().selectSingleObject("/");

Assert.assertNotNull(obj);

Assert.assertTrue(obj instanceof Node);

Assert.assertEquals(s.getRootNode(), obj);

{{< /highlight >}}

Söksyntaxen inspirerades av XPath, så de flesta koncept och syntax är liknande, sökningen syntax är kompatibel med URL så den kommer att användas i vår molnversion i framtiden. Vanligtvis består en syntax av en syntax**Prefixnamn villkor** / **Namnvillkor** /.

|**Prefix=**|**Beskrivning=**|
|:- |:- |
||Global väljare, varje ättling behandlas som rotnod för att utföra markeringen|
|/|Rotväljare, bara en förfader används för att söka upp.|
|Andra slag|Anta att det är ett namn, och välj objektet efter namn i globalt valläge|
Namnet är en sträng som matchar objektets namn, eller '*' används för att matcha vilket namn som helst. Villkoret är ett uttryck för att avgöra om att välja objektet, boolean operatörer (inte) och, jämförelseoperatörer >/<=/=/=! = stöds. För att komma åt en egenskap i tillståndsuttrycket används '@' prefix, e. g. @Name läser egenskapen Namn. En genvägssyntax för testtyp stöds av <Mesh>, Det här motsvarar [@Type = 'Mesh'], identifierare utan citat kommer att behandlas som en sträng.

**Välj alla noder med hjälp av global syntaxväljare:**

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

 **Välj en andra nivånod med en synlig förälder:**

 {{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}
