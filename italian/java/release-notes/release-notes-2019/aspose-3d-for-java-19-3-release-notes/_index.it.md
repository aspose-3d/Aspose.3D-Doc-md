---
title: Aspose.3D for Java 19.3 Note di rilascio
type: docs
weight: 100
url: /it/java/aspose-3d-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 19.3](https://repository.aspose.com/repo/com/aspose/aspose-xps/19.3/).

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-471 |XPath come metodi di indirizzamento degli oggetti|Nuova funzionalità|

## **Pubblico API e modifiche incompatibili arretrate**

Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for Java. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).

**Aggiunto il metodo selectSingleObject nella classe com.aspose.threed.Node**

{{< highlight "java" >}}

 /**

 * Select single object under current node using XPath-like query syntax.

 * @param path 

 * @throws ParseException ParseException will be thrown if the path contains malformed query.

 */

public A3DObject selectSingleObject(String path)

    throws ParseException;

{{< /highlight >}}

**Aggiunto metodo selectOggetti in classe com.aspose.threed.Node**

{{< highlight "java" >}}

 /**

 * Select multiple objects under current node using XPath-like query syntax.

 * @param path 

 * @throws ParseException ParseException will be thrown if the path contains malformed query.

 */

public ArrayList<A3DObject> selectObjects(String path)

    throws ParseException;

{{< /highlight >}}

Di seguito è riportato il codice di esempio per interrogare uno o più oggetti:

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

La sintassi della query è stata ispirata da XPath, quindi la maggior parte dei concetti e della sintassi sono simili, la sintassi della query è compatibile con l'URL, quindi verrà utilizzata nella nostra versione cloud in futuro. Di solito, una sintassi è composta da**Condizione del nome prefisso** / **Condizione del nome** /.

|**Prefisso =**|**Descrizione =**|
|:- |:- |
||Selettore globale, qualsiasi discendente viene trattato come nodo radice per eseguire la selezione|
|/|Selettore radice, solo un antenato serve a guardare in alto|
|Altro|Supponiamo che sia un nome e seleziona l'oggetto in base al nome in modalità selettore globale|
Il nome è una stringa che corrisponde al nome dell'oggetto o il carattere jolly "*" viene utilizzato per corrispondere a qualsiasi nome. La condizione è un'espressione per decidere se selezionare l'oggetto, sono supportati gli operatori booleani (non) e o gli operatori di confronto>/</>=/<=/=/!=. Per accedere a una proprietà nell'espressione di condizione, viene utilizzato il prefisso '@', ad esempio @ Name leggerà la proprietà Name. Una sintassi di collegamento per il tipo di test è supportata da <Mesh>, questa è equivalente a [@ Type = 'Mesh'], gli identificatori senza preventivo saranno trattati come una stringa.

**Seleziona tutti i nodi usando il selettore globale della sintassi:**

{{< highlight "java" >}}

 //<Node>

{{< /highlight >}}

Questa è la sintassi breve di:

{{< highlight "java" >}}

 //*[<Node>]

{{< /highlight >}}

O

{{< highlight "java" >}}

 //*[@Type = Node]

{{< /highlight >}}

 **Seleziona un nodo di secondo livello con un genitore visibile:**

 {{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}
