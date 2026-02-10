---
title: Licensing
type: docs
weight: 60
url: /it/net/licensing/
description: Panoramica dei requisiti di Licensing e delle limitazioni della versione di valutazione per l'elaborazione dei formati di file 3D in C#.
---
Panoramica dei requisiti di Licensing e delle limitazioni della versione di valutazione per l'elaborazione dei formati di file 3D in C#.

##  **Limitazioni della versione di valutazione**
Una versione di valutazione gratuita di Aspose.3D for .NET può essere scaricato dalla sezione download del sito Web di Aspose all'indirizzo: [Scarica Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
###  **Limitazione**
La versione di valutazione fornisce tutte le funzionalità tranne le seguenti:

- Gli utenti possono aprire/importare solo un massimo di 50 3D documenti su una scena.
- Ogni nodo non può avere più di 5 nodi figlio.
- Ogni nodo non può avere più di 2 entità allegate.
- Ogni geometria non può avere più di 2 elementi di vertice collegati.
- Ogni nodo non può avere più di 1 materiale.
- Gli utenti possono salvare solo un massimo di 50 3D documenti in una scena.
- Gli utenti vedranno anche una filigrana di valutazione nelle immagini renderizzate e in tutti gli altri file di output.

{{% alert color="primary" %}} 
Se usi Aspose.3D senza una licenza adeguata, potrebbe scattare `Aspose.ThreeD.TrialException` quando l'utilizzo ha raggiunto le restrizioni senza licenza, puoi disattivare l'eccezione:

* [Buy a full featured license](https://purchase.aspose.com/buy).
* Richiedi una licenza temporanea di 30 giorni, fai riferimento a [Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) Per ulteriori informazioni.
.
* Imposta `Aspose.ThreeD.TrialException.SuppressTrialException` a `true`, il `TrialException` non verrà aumentato durante la chiamata `Open/Save` sulla scena, ma le restrizioni di cui sopra non verranno revocate.
* Usa manualmente un blocco `try/catch` su `Scene.Open/Save`, questa eccezione è solo una notifica, ignorarla non influirà sul caricamento/salvataggio della scena.

{{% /alert %}} 

##  **Applicare la licenza utilizzando file o oggetto Stream**
La licenza può essere caricata da [File](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) o [Oggetto di flusso](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET proverà a trovare la licenza nelle seguenti posizioni:

1. Percorso esplicito.
1. La cartella che contiene Aspose.3D.dll.
1. La cartella che contiene l'assembly che ha chiamato Aspose.3D.dll.
1. La cartella che contiene l'assembly di voce (il tuo. Exe).
1. Una risorsa incorporata nell'assembly che ha chiamato Aspose.3D.dll.

Il modo più semplice per impostare una licenza è inserire il file di licenza nella stessa cartella del file Aspose.3D.dll e specificare il nome del file, senza un percorso, come mostrato nell'esempio seguente.

{{% alert color="primary" %}} 

Se usi altri Aspose for .NET API insieme a Aspose.3D for .NET, specifica lo spazio dei nomi per la licenza come `Aspose.ThreeD.License`.

{{% /alert %}} 
###  **Caricamento di una licenza dal file**
Il modo più semplice per applicare una licenza è inserire il file di licenza nella stessa cartella del file Aspose.3D.dll e specificare solo il nome del file senza un percorso.

{{% alert color="primary" %}} 

Quando chiami il metodo `SetLicense`, il nome della licenza che passi dovrebbe essere quello del file di licenza. Ad esempio, se modifichi il nome del file di licenza in "Aspose.3D.lic.xml" passa il nome del file al metodo `threeD.SetLicense(…)`.

{{% /alert %}} 

**Esempio:**

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
###  ` `**Caricamento di una licenza da un oggetto Stream**
L'esempio seguente mostra come caricare una licenza da un flusso.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Aspose.ThreeD.License license = new Aspose.ThreeD.License();
FileStream myStream = new FileStream("Aspose._3D.lic", FileMode.Open);
license.SetLicense(myStream);

{{< /highlight >}}
##  **Applica la licenza utilizzando la risorsa incorporata**
Un modo per applicare una licenza è impostarla [Utilizzando un file o un oggetto stream](). Un altro modo preciso per impacchettare la licenza con la tua applicazione e assicurarti che non vada persa è includerla come risorsa incorporata in uno degli assembly che chiama la DLL del componente (inclusa in Aspose.3D).

Per includere il file di licenza come risorsa incorporata:

1. In Visual Studio .NET, includere il file di licenza (.lic) nel progetto selezionando**File**, Allora**Aggiungi elemento esistente**E finalmente**Aggiungi**.
1. Selezionare il file in Solution Explorer.
1. Impostare il**Costruisci azione**A**Risorsa incorporata**Nella finestra Proprietà.
1. Per accedere alla licenza incorporata nell'assembly (come risorsa incorporata), basta aggiungere il file di licenza come risorsa incorporata al progetto e passare il nome del file di licenza al metodo SetLicense. La classe Licenza trova automaticamente il file di licenza nelle risorse incorporate. Non è necessario chiamare i metodi GetExecutingAssembly e GetManifestResourceStream della classe System.Reflection.Assembly nel Framework Microsoft .NET.

Il seguente frammento di codice viene utilizzato per impostare la licenza.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Instantiate the License class
Aspose.ThreeD.License license = new Aspose.ThreeD.License();

// Pass only the name of the license file embedded in the assembly
license.SetLicense("Aspose._3D.lic");

{{< /highlight >}}
##  **Applica licenza misurata**
Aspose.3D for .NET API consente agli sviluppatori di applicare la licenza misurata. È un nuovo meccanismo di licenza. Il nuovo meccanismo di licenza sarà utilizzato insieme al metodo di licenza esistente. I clienti che desiderano essere fatturati in base all'utilizzo delle funzionalità API possono utilizzare la licenza misurata. Per maggiori dettagli, fai riferimento alla sezione [Domande frequenti su Licensing misurate](https://purchase.aspose.com/faqs/licensing/metered).

È stata aggiunta una nuova classe [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) per applicare la chiave misurata. Questo esempio di codice dimostra come impostare chiavi pubbliche e private con misurazione:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize a Metered license class object
Aspose.ThreeD.Metered metered = new Aspose.ThreeD.Metered();
// Set public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
