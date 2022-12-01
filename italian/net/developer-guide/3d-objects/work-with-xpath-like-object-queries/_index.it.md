---
title: Lavora con le query degli oggetti simili a XPath
type: docs
weight: 120
url: /it/net/work-with-xpath-like-object-queries/
description: Utilizzando Aspose.3D for .NET, è possibile selezionare uno o più oggetti sotto il nodo corrente utilizzando la sintassi di query XPath-Like. La sintassi della query è stata ispirata da XPath, quindi la maggior parte dei concetti e della sintassi sono simili, la sintassi della query è compatibile con l'URL, quindi verrà utilizzata nella nostra versione cloud in futuro.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.3 o maggiore.

{{% /alert %}} 
## **Lavora con le query degli oggetti simili a XPath**
Utilizzando Aspose.3D for .NET, è possibile selezionare uno o più oggetti sotto il nodo corrente utilizzando la sintassi di query XPath-Like. La sintassi della query è stata ispirata da XPath, quindi la maggior parte dei concetti e della sintassi sono simili, la sintassi della query è compatibile con l'URL, quindi verrà utilizzata nella nostra versione cloud in futuro. Di solito, una sintassi è composta da**Condizione del nome prefisso** / **Condizione del nome** /.

|**Prefisso =**|**Descrizione =**|
|:- |:- |
|// |Selettore globale, qualsiasi discendente viene trattato come nodo radice per eseguire la selezione|
|/|Selettore radice, solo un antenato serve a guardare in alto|
|Altro|Supponiamo che sia un nome e seleziona l'oggetto in base al nome in modalità selettore globale|
Il nome è una stringa che corrisponde al nome dell'oggetto o il carattere jolly `*` viene utilizzato per corrispondere a qualsiasi nome. La condizione è un'espressione per decidere se selezionare l'oggetto, sono supportati gli operatori booleani (non) e o, gli operatori di confronto `>/</>=/<=/=/!=`. Per accedere a una proprietà nell'espressione di condizione, viene utilizzato il prefisso '@', ad esempio `@Name` leggerà la proprietà Name. Una sintassi di collegamento per il tipo di test è supportata dallo `<Mesh>`, equivalente allo `[@Type = 'Mesh']`, gli identificatori senza preventivo saranno trattati come una stringa.
### **Seleziona tutti i nodi usando il selettore globale della sintassi**
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
### **Selezionare un nodo di secondo livello con un genitore visibile**
{{< highlight "java" >}}

 //<Node>[@Visible]/<Node>

{{< /highlight >}}

Di seguito è riportato il codice di esempio per interrogare uno o più oggetti:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-XPathLikeObjectQueries-XPathLikeObjectQueries.cs" >}}
