---
title: Aspose.3D for .NET 19,3 Utgivning
type: docs
weight: 100
url: /sv/net/aspose-3d-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,3](https://www.nuget.org/packages/Aspose.3D/19.3.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-471 |XPath- liknande objekt adresseringsmetoder|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
#### **Tillagd metod väljSingleObject i klass com.aspose.3reed.Node.**
{{< highlight "java" >}}

 /// <summary>

/// Select single object under current node using XPath-like query syntax.

/// </summary>

/// <param name="path"></param>

/// <exception cref="ParseException">ParseException will be thrown if the path contains malformed query.</exception>

/// <returns></returns>

public Aspose.ThreeD.A3DObject SelectSingleObject(string path)

{{< /highlight >}}
#### **Tillagd metod SelectObjekts i klass Aspose.ThreeD.Node**
{{< highlight "java" >}}

 /// <summary>

/// Select multiple objects under current node using XPath-like query syntax.

/// </summary>

/// <param name="path"></param>

/// <exception cref="ParseException">ParseException will be thrown if the path contains malformed query.</exception>

/// <returns></returns>

public System.Collections.Generic.List<Aspose.ThreeD.A3DObject> SelectObjects(string path)

{{< /highlight >}}

Följande är provkoden för att fråga ett eller flera objekt:

{{< highlight "java" >}}

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

Assert.AreEqual(2, objects.Count);

Assert.IsInstanceOf<Camera>(objects[0]);

Assert.IsInstanceOf<Light>(objects[1]);

//Select single camera object under the child nodes of node named 'c' under the root node

var c1 = s.RootNode.SelectSingleObject("/c/*/<Camera>");

Assert.IsNotNull(c1);

// Select node named 'a1' under the root node, even if the 'a1' is not a directly child node of the 

var obj = s.RootNode.SelectSingleObject("a1");

Assert.AreEqual("a1", obj.Name);

//Select the node itself, since the '/' is selected directly on the root node, so the root node is selected.

obj = s.RootNode.SelectSingleObject("/");

Assert.NotNull(obj);

Assert.IsInstanceOf<Node>(obj);

Assert.AreEqual(s.RootNode, obj);

{{< /highlight >}}

Söksyntaxen inspirerades av XPath, så de flesta koncept och syntax är liknande, sökningen syntax är kompatibel med URL så den kommer att användas i vår molnversion i framtiden. Vanligtvis består en syntax av en syntax**Prefixnamn villkor** / **Namnvillkor** /.

|**Prefix=**|**Beskrivning=**|
|:- |:- |
||Global väljare, varje ättling behandlas som rotnod för att utföra markeringen|
|/|Rotväljare, bara en förfader används för att söka upp.|
|Andra slag|Anta att det är ett namn, och välj objektet efter namn i globalt valläge|
Namnet är en sträng som matchar objektets namn, eller '*' används för att matcha vilket namn som helst. Villkoret är ett uttryck för att avgöra om att välja objektet, boolean operatörer (inte) och, jämförelseoperatörer >/<=/=/=! = stöds. För att komma åt en egenskap i tillståndsuttrycket används '@' prefix, e. g. @Name läser egenskapen Namn. En genvägssyntax för testtyp stöds av <Mesh>, Det här motsvarar [@Type = 'Mesh'], identifierare utan citat kommer att behandlas som en sträng.
#### **Välj alla noder med hjälp av global syntaxväljare:**
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
#### **Välj en andra nivånod med en synlig förälder:**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}
