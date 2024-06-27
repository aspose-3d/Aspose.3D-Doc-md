---
title: MappingMode e ReferenceMode spiegano
type: docs
weight: 10
url: /it/net/mapping-mode-and-reference-mode-explains
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono definire mesh con vari elementi di dati vertici, qui spieghiamo come mappare i dati al componente mesh e riottenere i dati.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori possono definire mesh con vari elementi di dati del vertice, inclusi normali, colori e pesi. Aspose.3D offre due meccanismi per ottimizzare il riutilizzo dei dati: `MappingMode` e `ReferenceMode`. Questi meccanismi sono progettati per ridurre al minimo l'impronta di memoria delle mesh, in particolare nei formati avanzati come FBX e USD. MappingMode consente una mappatura efficiente dei dati dei vertici ai componenti mesh, mentre ReferenceMode facilita il riferimento dei dati degli elementi dei vertici su più componenti mesh. Insieme, queste funzionalità migliorano le prestazioni e l'efficienza della memoria, rendendo Aspose.3D un potente strumento per gestire modelli complessi di 3D in applicazioni .NET.

{{% /alert %}}



###  `MappingMode` spiega

 `MappingMode` determina il modo in cui i dati dell'elemento vengono mappati sulla superficie della geometria in Aspose.3D for .NET. Fornisce vari modi per definire questa mappatura:

1. **Punto di controllo**, Ogni elemento di dati viene mappato al punto di controllo della geometria. Questa modalità garantisce che ogni punto di controllo, che definisce la forma della geometria, sia associato a un elemento di dati specifico.
1. **Poligonvertex**, I dati vengono mappati al vertice di un poligono. Nei casi in cui un punto di controllo è condiviso da più poligoni, ogni istanza del punto di controllo, come appare in poligoni diversi, avrà i propri dati distinti. Ciò garantisce che anche i punti di controllo condivisi possano avere dati univoci quando fungono da vertici per poligoni diversi.
1. **Poligono**, I dati vengono mappati all'intero poligono. Ciò significa che tutti i vertici di un poligono condividono lo stesso elemento di dati. Questa modalità è utile quando è necessario applicare dati uniformi su tutta la superficie poligonale, garantendo la coerenza all'interno del poligono.
1. **Bordo**, I dati vengono mappati ai bordi della geometria. Ogni endpoint di un bordo condivide gli stessi dati, fornendo un modo per applicare dati uniformi ai bordi consentendo al contempo dati distinti per bordi diversi. Ciò può essere particolarmente utile per definire caratteristiche specifiche dei bordi, come i valori di piega o gli attributi basati sui bordi
1. **AllSame**, Un singolo elemento di dati viene mappato all'intera superficie della geometria. Indipendentemente dal fatto che i dati vengano interpretati come punti di controllo, vertici poligonali o endpoint di bordo, lo stesso valore di dati viene applicato in modo uniforme a tutti gli elementi. Questa modalità è ideale per gli scenari in cui è necessario mantenere un valore costante durante l'intera geometria, garantendo un attributo uniforme sull'intero modello 3D.




###  `ReferenceMode` spiega
 `ReferenceMode` definisce se riutilizzare i dati per indici, ci sono tre politiche per `ReferenceMode`:

1.**Diretto**I dati vengono referenziati direttamente e memorizzati nella proprietà `Data` di `VertexElement`.
1.**IndexToDirect**, I dati sono referenziati dall'indice, quindi accessibili dall'indice nell'elenco dei dati di `VertexElement`.
1.**Indice**, I dati sono referenziati solo dall'indice, ora solo i `VertexElementMaterial` utilizzano questa modalità di riferimento, questa è simile a `IndexToDirect` ma le differenze sono i materiali definiti sotto la proprietà `Node` `Materials`, non in `VertexElementMaterial`, tutti i `VertexElement` funzionano solo con dati primitivi.



Ad esempio, data una definizione di un cubo:

{{< highlight "csharp" >}}
var cube = new Mesh();
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};
cube.ControlPoints.AddRange(controlPoints);

// Front face (Z+)
cube.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
cube.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
cube.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
cube.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
cube.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
cube.CreatePolygon(new int[] { 3, 2, 6, 7 });

var vertexColor = (VertexElementVertexColor) cube.CreateElement(VertexElementType.VertexColor);
vertexColor.MappingMode = MappingMode.ControlPoint;
var red = new Vector4(1, 0, 0, 1);
var green = new Vector4(0, 1, 0, 1);
var blue = new Vector4(0, 0, 1, 1);
var white = new Vector4(1, 1, 1, 1);

{{< /highlight >}}

Se vuoi assegnare il rosso ai punti di controllo 0 e 1, il verde per controllare i punti 2 e 3, il blu per controllare i punti 4 e 5 e il bianco per controllare i punti 6 e 7, puoi ottenere questo risultato con il seguente approccio:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.Direct;
vertexColor.Data.Add(red); // 0
vertexColor.Data.Add(red); // 1
vertexColor.Data.Add(green); // 2
vertexColor.Data.Add(green); // 3
vertexColor.Data.Add(blue); // 4
vertexColor.Data.Add(blue); // 5
vertexColor.Data.Add(white); // 6
vertexColor.Data.Add(white); // 7
{{< /highlight >}}

Per assegnare i colori ai punti di controllo in modo efficiente e ridurre il consumo di memoria, è possibile utilizzare gli indici per fare riferimento ai colori. Definendo i colori separatamente e facendo quindi riferimento ad essi con gli indici, è possibile ridurre al minimo la ridondanza. Ecco come puoi ottenere questo:

In primo luogo, definire 4 colori nel tipo Vector4 per i colori unici, e quindi utilizzare un array di 8 indici per assegnare questi colori a ciascun punto di controllo:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

In questo approccio:

1. Definisci colori unici: solo 4 colori sono definiti (rosso, verde, blu, bianco) come istanze Vector4.
1. Creare un array di indici di colore: un array di 8 indici viene utilizzato per fare riferimento a questi 4 colori per ogni punto di controllo.
1. Mappa i colori utilizzando gli indici: facendo riferimento ai colori attraverso gli indici, riduci il consumo di memoria, poiché ogni colore viene memorizzato una volta e riutilizzato su più punti di controllo.

Questo metodo ottimizza l'utilizzo della memoria riducendo l'archiviazione ridondante dei dati, rendendo il tuo modello 3D più efficiente.