---
title: Aspose.3D Document Object Model (DOM)
type: docs
weight: 20
url: "/it/nodejs-java/aspose-3d-document-object-model"
description: "Ogni scena 3D può comprendere un numero qualsiasi di viewport. Utilizzando Aspose.3D per l'API nodejs-java, gli sviluppatori possono catturare uno o più viewport in un singolo screenshot. Possono renderlo in un'applicazione GUI basata su nodejs-java o in un'immagine."
---

L'Aspose.3D Document Object Model (DOM) è una potente rappresentazione in memoria di una scena 3D. Fornisce agli sviluppatori la possibilità di leggere, manipolare e modificare programmaticamente il contenuto e la formattazione di una scena 3D.

In questa sezione, esploreremo le classi chiave del DOM Aspose.3D e le loro relazioni. Utilizzando queste classi, è possibile accedere programmaticamente a vari elementi all'interno di una scena 3D.

Esaminiamo ora le classi principali del DOM Aspose.3D:

* **Scene**: La classe Scene rappresenta la radice della gerarchia della scena 3D. Funge da contenitore per tutti gli altri elementi e fornisce metodi per manipolare l'intera scena.
* **Node**: I nodi sono i mattoni di una scena 3D. Rappresentano singoli oggetti o entità all'interno della scena, come mesh, luci, telecamere o gruppi. I nodi possono essere trasformati, animati e texturizzati.
* **Entities**: La classe Entities comprende un'ampia gamma di oggetti ed elementi che costituiscono una scena 3D. Include entità come mesh, luci, telecamere, profili e altro ancora. Queste entità fungono da mattoni, consentendoti di creare scene complesse combinandole e manipolandole programmaticamente. La categoria Entities fornisce accesso e controllo su questi elementi fondamentali di una scena 3D.
* **Materials**: La classe Materials si concentra sulla definizione delle proprietà visive degli oggetti all'interno di una scena 3D. Fornisce strumenti per creare, modificare e controllare programmaticamente i materiali, che determinano come la luce interagisce con le superfici. Regolando proprietà come colore, texture, trasparenza e riflessione, è possibile ottenere vari effetti visivi e personalizzare l'aspetto dei modelli 3D.
* **Animations**: La classe Animation si concentra sulla creazione e sul controllo del movimento e delle trasformazioni all'interno di una scena 3D. Consente di definire e manipolare programmaticamente le animazioni, consentendo agli oggetti di muoversi, ruotare, scalare o modificare le proprietà nel tempo. Con questa categoria, è possibile aggiungere elementi dinamici e interattivi alle scene 3D.

Utilizzando le classi del DOM Aspose.3D menzionate in precedenza, è possibile interagire e manipolare programmaticamente il contenuto e la struttura di una scena 3D. Ciò fornisce flessibilità e controllo quando si lavora con modelli 3D nelle applicazioni.

## Struttura della scena

Quando Aspose.3D legge un file 3D in memoria, genera oggetti di vari tipi per rappresentare i diversi elementi all'interno della scena 3D.

La struttura della scena in Aspose.3D segue il pattern di progettazione composite, che offre flessibilità e organizzazione:

* I nodi fungono da contenitori che possono contenere altri nodi, consentendo di raggruppare diversi oggetti all'interno della scena.
* Ogni nodo può avere la propria trasformazione, che si applica anche ai suoi nodi figlio.
* Tutti i tipi di entità spaziali in Aspose.3D devono essere posizionati sotto un'istanza Node. Ciò garantisce che oggetti come mesh, luci, telecamere e altri elementi siano organizzati nella gerarchia della scena.
* I nodi possono contenere più materiali e la relazione tra poligoni e materiali collegati a un nodo viene gestita utilizzando il concetto di `VertexElementMaterial` all'interno dell'oggetto Mesh.

![Gerarchia della scena](scene.png)

## Entità spaziali
Tutte le entità spaziali in Aspose.3D ereditano dalla classe `Entity`, fungendo da elementi costitutivi fondamentali per la costruzione di ambienti virtuali. Aspose.3D categorizza queste entità in diverse categorie principali, ciascuna con il proprio scopo e funzionalità specifici.

![Entità](entity.png)

* **Primitive**: La classe `Primitive` funge da classe base per tutte le geometrie procedurali 3D in Aspose.3D, come `Cylinder`, `Torus` e `Sphere`. Queste geometrie possono essere definite utilizzando un set minimo di parametri, rendendo conveniente creare forme 3D di base.
* **Geometry**: Le geometrie in Aspose.3D in genere consistono di vertici, bordi e poligoni che definiscono la forma e la struttura di un oggetto 3D. Questa categoria comprende un'ampia gamma di geometrie complesse utilizzate per rappresentare vari oggetti all'interno di una scena 3D.
* **Profile**: I profili, simili ai primitivi, definiscono contorni chiusi 2D nel piano x-y. Forniscono un modo per creare forme 2D che possono essere estrusi per generare geometrie 3D corrispondenti. I profili vengono spesso utilizzati come punto di partenza per la progettazione di geometrie 3D.
* **Text**: Aspose.3D include la possibilità di generare profili dal testo utilizzando un font specificato. Questa funzionalità consente di creare profili a forma di lettere, numeri o qualsiasi altro contenuto testuale, aggiungendo un elemento di personalizzazione o branding ai modelli 3D.

![2D profile types](profiles.png)

## Camera e light types

![Camera and light](frustums.png)

## Material types

Aspose.3D fornisce supporto per vari tipi di materiali, tra cui materiale Lambert, materiale Phong, materiale PBR, materiale PBR speculare e materiale shader (disponibile solo nei file FBX).

Ogni materiale in Aspose.3D può avere proprietà e attributi diversi che definiscono il suo aspetto e il suo comportamento all'interno di una scena 3D. Questi materiali possono essere collegati a istanze di texture, migliorando le loro caratteristiche visive.

Le texture in Aspose.3D sono associate a un attributo materiale specifico. Il tipo di texture combina le definizioni dei parametri per la sorgente dell'immagine e il sampler della texture. Utilizzando le texture, è possibile applicare schemi, colori e altri effetti visivi dettagliati alle superfici dei modelli 3D.

Con il supporto di un'ampia gamma di tipi di materiali e la possibilità di collegare texture, Aspose.3D offre flessibilità nella creazione di materiali visivamente accattivanti e realistici per le scene 3D.

![Material types](materials.png)

## Animation objects relationship
Aspose.3D fornisce supporto a livello di dati per l'animazione e il supporto per i calcoli è attualmente in fase di sviluppo.

In Aspose.3D, una scena può contenere più oggetti AnimationClip. Ogni clip di animazione può consistere in più nodi di animazione. Il nodo di animazione segue il pattern di progettazione composite, consentendo la creazione di strutture gerarchiche con nodi di animazione secondari.

I nodi di animazione possono essere associati a punti di binding, che definiscono le proprietà dell'oggetto di destinazione che verranno animate. I vettori sono tipi di dati comunemente utilizzati in molte proprietà di entità. Pertanto, i punti di binding possono avere canali di animazione diversi per aggiornare i canali specifici del vettore in modo indipendente. Ogni canale contiene una sequenza di fotogrammi chiave che definisce come il valore viene animato nel tempo.

Questo sistema fornisce un framework flessibile per l'animazione di oggetti all'interno di una scena. Definendo clip di animazione, nodi, punti di binding e canali, è possibile creare animazioni complesse e dinamiche che influiscono su varie proprietà delle entità nella scena 3D.

Sebbene Aspose.3D attualmente supporti l'animazione a livello di dati, lo sviluppo in corso si concentra sull'espansione del supporto per i calcoli, che migliorerà le capacità di creazione e manipolazione delle animazioni all'interno del framework.

![Animations](animations.png)

Una scena con animazioni può avere questo tipo di struttura:

![Animations Sample](animation_relations.png)