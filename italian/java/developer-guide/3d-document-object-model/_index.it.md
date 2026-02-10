---
title: Aspose.3D Document Object Model (DOM)
type: docs
weight: 20
url: /it/java/aspose-3d-document-object-model
description: Ogni scena 3D può comprendere un numero qualsiasi di visualizzazioni. Utilizzando Aspose.3D for Java API, gli sviluppatori possono acquisire una o più visualizzazioni in un singolo screenshot. Possono renderizzarlo nell'applicazione Java o in un'immagine basata sulla GUI.
---
Il Aspose.3D Document Object Model (DOM) è una potente rappresentazione in memoria di una scena 3D. Fornisce agli sviluppatori la possibilità di leggere, manipolare e modificare il contenuto e la formattazione di una scena 3D a livello di programmazione.

In questa sezione, esploreremo le classi chiave del Aspose.3D DOM e le loro relazioni. Utilizzando queste classi, è possibile ottenere l'accesso programmatico a vari elementi all'interno di una scena 3D.

Andiamo ad approfondire le classi principali di Aspose.3D DOM:

* **Scena**: La classe Scene rappresenta la radice della gerarchia di scene 3D. Serve come contenitore per tutti gli altri elementi e fornisce metodi per manipolare la scena generale.
* **Nodo**: I nodi sono gli elementi costitutivi di una scena 3D. Rappresentano singoli oggetti o entità all'interno della scena, come mesh, luci, telecamere o gruppi. I nodi possono essere trasformati, animati e strutturati.
* **Entità**: Le classi Entities comprendono un'ampia gamma di oggetti ed elementi che compongono una scena 3D. Include entità come mesh, luci, telecamere, profili e altro ancora. Queste entità fungono da elementi costitutivi, consentendo di creare scene complesse combinandole e manipolandole a livello di programmazione. La categoria Entità fornisce l'accesso e il controllo su questi elementi fondamentali di una scena 3D.
* **Materiali**: Le classi Materiali ruotano attorno alla definizione delle proprietà visive degli oggetti all'interno di una scena 3D. Fornisce strumenti per creare, modificare e controllare i materiali a livello di programmazione, che determinano il modo in cui la luce interagisce con le superfici. Regolando proprietà come colore, consistenza, trasparenza e riflessione, puoi ottenere vari effetti visivi e personalizzare l'aspetto dei tuoi modelli 3D.
* **Animazioni**: Le classi di animazione si concentrano sulla creazione e il controllo di movimenti e trasformazioni all'interno di una scena 3D. Consente di definire e manipolare animazioni a livello di programmazione, consentendo agli oggetti di spostarsi, ruotare, scalare o modificare le proprietà nel tempo. Con questa categoria, puoi portare elementi dinamici e interattivi alle tue scene da 3D.

Utilizzando le classi DOM Aspose.3D sopra menzionate, puoi interagire e manipolare il contenuto e la struttura di una scena 3D in modo programmatico. Questo fornisce flessibilità e controllo quando si lavora con i modelli 3D nelle applicazioni.


## Struttura della scena

Quando Aspose.3D legge un file 3D in memoria, genera oggetti di vario tipo per rappresentare i diversi elementi all'interno della scena 3D.


La struttura della scena in Aspose.3D segue il modello di progettazione composita, che offre flessibilità e organizzazione:

 * Il nodo funge da contenitori che possono contenere altri nodi, consentendo il raggruppamento di oggetti diversi all'interno della scena.
 * Ogni nodo può avere una propria trasformazione, che si applica anche ai suoi nodi figlio.
 * Tutti i tipi di entità spaziali in Aspose.3D devono essere inseriti in un'istanza di Nodo. Ciò garantisce che oggetti come mesh, luci, telecamere e altri elementi siano organizzati all'interno della gerarchia delle scene.
 * I nodi possono contenere più materiali e la relazione tra poligoni e materiali collegati a un nodo viene indirizzata utilizzando il concetto `VertexElementMaterial` all'interno dell'oggetto Mesh.


! [Gerarchia della scena](scene.png)


## Entità spaziali
Tutte le entità spaziali entro Aspose.3D ereditano dalla classe `Entity`, fungendo da elementi costitutivi fondamentali per la costruzione di ambienti virtuali. Aspose.3D categorizza queste entità in diverse categorie principali, ognuna con il proprio scopo e funzionalità specifici.

! [Entità](entity.png)

* **Primitivo**La classe `Primitive` funge da classe base per tutte le geometrie 3D procedurali entro Aspose.3D, ad esempio `Cylinder`, `Torus` e `Sphere`. Queste geometrie possono essere definite utilizzando un set minimo di parametri, rendendo conveniente la creazione di forme di base di 3D.
* **Geometria**: Geometrie in Aspose.3D in genere sono costituiti da vertici, bordi e poligoni che definiscono la forma e la struttura di un oggetto 3D. Questa categoria comprende un'ampia gamma di geometrie complesse utilizzate per rappresentare vari oggetti all'interno di una scena 3D.
* **Profilo**: I profili, simili alle primitive, definiscono i contorni chiusi 2D nel piano x-y. Forniscono un modo per creare forme 2D che possono essere estruse per generare geometrie corrispondenti di 3D. I profili vengono spesso utilizzati come punto di partenza per la creazione di oggetti 3D più complessi.
* **Curva**: A differenza dei profili, le curve possono essere aperte o non collegate. Vengono utilizzati per definire percorsi spaziali in 3D. Le curve forniscono un mezzo per creare percorsi flessibili e personalizzabili che gli oggetti possono seguire in un ambiente 3D.
* **Estrusione**: Le estrusioni sono una tecnica procedurale impiegata per costruire geometrie di 3D utilizzando profili e curve. Applicando l'estrusione a un profilo o una curva, è possibile generare una forma 3D estendendo il profilo o la curva lungo una direzione specificata. Questo approccio consente la creazione di geometrie più complesse e dinamiche.
* **Frustum**: La categoria frustum include oggetti come luci e fotocamere. Frustum definisce il volume di visualizzazione e la prospettiva in una scena 3D. Le telecamere utilizzano i frustum per determinare la parte della scena che sarà visibile, mentre le luci utilizzano i frustum per definire la regione entro la quale illuminano la scena.

Queste principali categorie di entità in Aspose.3D comprendono una varietà di entità che svolgono un ruolo essenziale nella costruzione e nella rappresentazione di ambienti virtuali, fornendo un kit di strumenti versatile per la creazione e la manipolazione di 3D scene.


### Tipi di geometria

! [Tipi di geometria](geometries.png)

Aspose.3D contiene molti tipi di geometria:


* `Mesh` mesh poligono compatibile con lo strumento di creazione.
* `PointCloud` nuvola di punti.
* `NurbsSurface` Superfici B-Spline razionali non uniformi.
* Superficie `Patch` definita da un insieme di punti di controllo e funzioni di fusione.
* `TriMesh` Render mesh a triangolo compatibile con API.


I più importanti sono `Mesh` e `TriMesh`, le differenze sono nella tabella:

|Caratteristica| `Mesh` | `TriMesh` |
| ---     |---     |---        |
|Poligono non triangolare|Sì|No|
|Facile da modificare|Sì|No|
|Riutilizzo dell'indice dei dati|Sì|No|
|Cache della CPU amichevole|No|Sì|
|Rendering API amichevole|No|Sì|
|Disposizione fissa della memoria|No|Sì|

Le classi derivate da `Geometry` sono progettate per la modifica e la creazione di contenuti mentre `TriMesh` è progettato per il rendering.

A `Geometry` è costituito da punti di controllo e `VertexElement` che definiscono i dati extra per il vertice del punto di controllo/edge/polygon/polygon, `Geometry` può contenere zero o più `VertexElement`, le sottoclassi concrete di `Geometry` hanno implementato diversi metodi per la modellazione e rappresentare le geometrie di 3D.


! [Tipi di geometria](mesh.png)


È possibile creare manualmente un elemento vertice e assegnare dati per esso. Il seguente esempio di codice mostra come farlo:

{{< highlight "java" >}}
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}

### Tipi di geometria primitiva


Aspose.3D fornisce una serie di tipi di geometria primitiva predefiniti che seguono regole e algoritmi specifici per generare modelli 3D. Questi tipi primitivi semplificano il processo di creazione di geometrie 3D rispetto all'utilizzo di tipi di geometria più complessi.

I tipi primitivi predefiniti disponibili in Aspose.3D includono:

*  `Box`: La primitiva scatola consente di creare forme cuboidi rettangolari definite dalla loro larghezza, altezza e profondità.
* Cilindro: con il cilindro primitivo, è possibile generare forme cilindriche specificando il raggio e l'altezza. Questo è utile per creare oggetti come tubi o colonne.
*  `Dish`: Il piatto primitivo consente la creazione di geometrie a forma di piatto, comunemente usate per rappresentare oggetti come ciotole o antenne paraboliche.
*  `Plane`: Il piano primitivo genera superfici piane definite dalla loro larghezza e lunghezza. Viene spesso utilizzato come base o aereo terrestre in 3D scene.
*  `Pyramid`: Con la piramide primitiva, puoi creare geometrie a forma di piramide caratterizzate dalle dimensioni e dall'altezza della base. Questo è utile per costruire oggetti come edifici o piramidi.
*  `Torus`: Il toro primitivo ti consente di generare geometrie a forma di ciambella con raggi specificati per i cerchi maggiore e minore. È adatto per la creazione di oggetti simili ad anelli o pneumatici.
*  `RectangularTorus`: Il toro primitivo rettangolare produce geometrie simili a tori con sezioni trasversali rettangolari invece di quelle circolari. Fornisce ulteriore flessibilità per la creazione di forme uniche.
*  `Sphere`: La sfera primitiva genera geometrie perfettamente rotonde in base al raggio specificato. Questo è utile per creare oggetti come pianeti o palle.

Utilizzando questi tipi primitivi predefiniti in Aspose.3D, puoi creare facilmente un'ampia gamma di geometrie di base di 3D. Questo semplifica il processo di modellazione e ti consente di modellare e assemblare rapidamente oggetti all'interno delle tue scene da 3D.

! [Tipi di geometria primitiva](primitives.png)

Il seguente esempio di codice mostra come creare una sfera con raggio specificato:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java

        // initialize a scene
        Scene scene = new Scene();
        // initialize a Sphere
        Sphere sphere = new Sphere();
        // set radius
        sphere.setRadius(10);
        // add sphere to the scene
        scene.getRootNode().createChildNode(sphere);
        // save scene
        scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}


### Tipi di estrusione

L'estrusione può essere utilizzata per creare una varietà di oggetti complessi 3D, è un metodo fondamentale nella modellazione 3D che prevede l'estensione di un profilo 2D lungo una curva per creare un oggetto 3D.

In Aspose.3D abbiamo fornito 3 tipi di estrusione:

* `LinearExtrusion` L'estrusione lineare prende un profilo 2D come input ed estende la forma nella terza dimensione.
* `RevolvedAreaSolid` Questa classe rappresenta un modello solido ruotando una sezione trasversale fornita da un profilo attorno a un asse.
* `SweptAreaSolid` Questa classe rappresenta un modello solido mediante uno schema di rappresentazione ampia che consente a una sezione trasversale del profilo 2D di attraversare lo spazio.


! [Estrusioni](extrusions.png)

L'esempio di codice seguente mostra come creare un'estrusione lineare da un profilo di testo:

{{< highlight "java" >}}
    // Load font from bytes
    var font = FontFile.parse(Files.readAllBytes(Paths.get("test-font.otf")));
    // Create a Text profile
    var text = new Text();
    text.setFont(font);
    text.setContent("Hello World");
    text.setFontSize(10.0f);
    // Extrude the profile to give it a thickness.
    var linear = new LinearExtrusion(text, 10).toMesh();
    // create a scene from the mesh and save it to stl file
    var scene = new Scene(linear);
    scene.save("test.stl");


{{< /highlight >}}


### Tipi di curva

In Aspose.3D, una curva rappresenta uno o più percorsi spaziali che possono assumere varie forme, come linee, curve NURBS o curve composte composte da più segmenti di curva. Le curve sono comunemente utilizzate insieme ai tipi di estrusione per creare forme dinamiche e intricate 3D.

Le curve possono essere impiegate per definire percorsi complessi che gli oggetti seguono in un ambiente 3D, consentendo movimenti fluidi e precisi. Utilizzando diversi tipi di curve e componendoli insieme, puoi ottenere percorsi spaziali versatili e personalizzabili per i tuoi modelli 3D.

Inoltre, alcuni formati di file supportati da Aspose.3D offrono anche la possibilità di importare ed esportare i dati della curva. Ciò consente di integrare perfettamente le curve create in applicazioni esterne o di condividere curve generate entro Aspose.3D con altri software.


! [Tipi di curva](curves.png)

## Tipi di profilo

Aspose.3D offre una gamma di profili 2D che possono essere utilizzati per creare forme o contorni chiusi all'interno di un ambiente 3D. Questi profili consentono la creazione di complesse strutture 2D che possono essere ulteriormente estruse o manipolate in geometrie 3D. Ecco alcune importanti implementazioni del profilo in Aspose.3D:

* `ParameterizedProfile`: Aspose.3D fornisce diverse implementazioni che offrono profili con forme standard. Questi profili predefiniti consentono la rapida creazione di forme comunemente utilizzate come cerchi, rettangoli e poligoni.

* `MirroredProfile`: Questo tipo di profilo consente di rispecchiare un profilo esistente lungo l'asse Y, creando una forma simmetrica. Fornisce un modo conveniente per generare profili equilibrati e visivamente accattivanti.

* `ArbitraryProfile`: Con l'implementazione del profilo arbitrario, puoi mappare una curva arbitraria per creare un profilo chiuso. Ciò offre flessibilità nella progettazione di forme personalizzate definendo una curva e convertendola in un profilo chiuso per ulteriori manipolazioni.

* `Text`: Aspose.3D include la possibilità di generare profili dal testo utilizzando un font specificato. Questa funzione ti consente di creare profili sotto forma di lettere, numeri o qualsiasi altro contenuto testuale, aggiungendo un elemento di personalizzazione o branding ai tuoi modelli 3D.

! [Tipi di profilo 2D](profiles.png)

### Tipi di fotocamera e luce

! [Macchina fotografica e luce](frustums.png)

## Tipi di materiale

Aspose.3D fornisce supporto per vari tipi di materiali, inclusi materiale Lambert, materiale Phong, materiale PBR, materiale speculare PBR e materiale shader (disponibile solo in file FBX).

Ogni materiale in Aspose.3D può avere diversi attributi e proprietà che ne definiscono l'aspetto e il comportamento all'interno di una scena 3D. Questi materiali possono essere collegati alle istanze di texture, migliorando le loro caratteristiche visive.

Texture in Aspose.3D sono associati a un attributo materiale specifico. Il tipo di texture combina le definizioni dei parametri per la sorgente dell'immagine e il campionatore di texture. Utilizzando le trame, puoi applicare modelli dettagliati, colori e altri effetti visivi alle superfici dei tuoi modelli 3D.

Con il supporto per una vasta gamma di tipi di materiali e la possibilità di collegare trame, Aspose.3D offre flessibilità nella creazione di materiali visivamente accattivanti e realistici per le tue scene 3D.

! [Tipi di materiale](materials.png)

L'esempio di codice seguente mostra come applicare un materiale PBR a una geometria:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}

## Relazione oggetti animazione
Aspose.3D fornisce supporto per l'animazione a livello di dati e il supporto per il calcolo è attualmente in fase di sviluppo.

In Aspose.3D, una scena può contenere più oggetti AnimationClip. Ogni clip di animazione può essere costituita da più nodi di animazione. Il nodo dell'animazione segue il modello di progettazione composito, consentendo la creazione di strutture gerarchiche con nodi di animazione secondaria.

I nodi di animazione possono essere associati ai punti di legame, che definiscono le proprietà dell'oggetto target che verrà animato. I vettori sono tipi di dati comunemente utilizzati in molte proprietà dell'entità. Pertanto, i punti di legame possono avere diversi canali di animazione per aggiornare i canali specifici del vettore in modo indipendente. Ogni canale contiene una sequenza di fotogrammi chiave che definisce come il valore viene animato nel tempo.

Questo sistema fornisce un framework flessibile per l'animazione di oggetti all'interno di una scena. Definendo clip di animazione, nodi, punti di associazione e canali, puoi creare animazioni complesse e dinamiche che influenzano varie proprietà delle entità nella scena 3D.

Mentre Aspose.3D attualmente supporta l'animazione a livello di dati, lo sviluppo continuo è incentrato sull'espansione del supporto per il calcolo, che migliorerà le capacità per la creazione e la manipolazione delle animazioni all'interno del framework.

! [Animazioni](animations.png)


Una scena con animazioni può avere questo tipo di struttura:


! [Campione di animazioni](animation_relations.png)