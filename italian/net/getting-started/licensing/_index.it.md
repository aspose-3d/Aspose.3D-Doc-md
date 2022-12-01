---
title: Licenze
type: docs
weight: 60
url: /it/net/licensing/
description: Panoramica dei requisiti di licenza e delle limitazioni della versione di valutazione per l'elaborazione dei formati di file 3D in C#.
---
Panoramica dei requisiti di licenza e delle limitazioni della versione di valutazione per l'elaborazione dei formati di file 3D in C#.

## **Limitazioni della versione di valutazione**
Una versione di valutazione gratuita dello Aspose.3D for .NET può essere scaricata dalla sezione download del sito Web dello Aspose all'indirizzo:[Scaricare Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
### **Limitazione**
La versione di valutazione fornisce tutte le funzionalità tranne le seguenti:

- Gli utenti possono aprire/importare solo un massimo di 50 3D documenti su una scena.
- Ogni nodo non può avere più di 5 nodi figlio.
- Ogni nodo non può avere più di 2 entità allegate.
- Ogni geometria non può avere più di 2 elementi di vertice collegati.
- Ogni nodo non può avere più di 1 materiale.
- Gli utenti possono salvare solo un massimo di 50 3D documenti in una scena.
- Gli utenti vedranno anche una filigrana di valutazione nelle immagini renderizzate e in tutti gli altri file di output.

{{% alert color="primary" %}} 
Se stai utilizzando Aspose.3D senza una licenza adeguata, potrebbe scattare un `Aspose.ThreeD.TrialException` quando l'utilizzo ha raggiunto le restrizioni senza licenza, puoi disattivare l'eccezione:

* [Acquista una licenza completa in primo piano](https://purchase.aspose.com/buy).
* Richiedi una licenza temporanea di 30 giorni, fai riferimento a [Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) Per ulteriori informazioni.
.
* Imposta 'Aspose.ThreeD.TrialException. SoppressTrialException' su 'vero', la 'Eccezione di triale' non verrà sollevata durante la chiamata 'Apri/Salva' sulla scena, ma le restrizioni di cui sopra non verranno revocate.
* Usa manualmente un blocco 'prova/cattura' su 'Scena. Apri/Salva', questa eccezione è solo una notifica, ignorarla non influirà sul caricamento/salvataggio della scena.

{{% /alert %}} 

## **Applicare la licenza utilizzando file o oggetto Stream**
La licenza può essere caricata da un[File](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile)O[Oggetto di flusso](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET cercherà di trovare la licenza nelle seguenti località:

1. Percorso esplicito.
1. La cartella che contiene Aspose.3D.dll.
1. La cartella che contiene l'assembly che ha chiamato Aspose.3D.dll.
1. La cartella che contiene l'assembly di voce (il tuo. Exe).
1. Una risorsa incorporata nell'assembly che ha chiamato Aspose.3D.dll.

Il modo più semplice per impostare una licenza è inserire il file di licenza nella stessa cartella del file Aspose.3D.dll e specificare il nome del file, senza un percorso, come mostrato nell'esempio seguente.

{{% alert color="primary" %}} 

Se si utilizza qualsiasi altro Aspose for .NET API insieme a Aspose.3D for .NET, si prega di specificare lo spazio dei nomi per la licenza come `Aspose.ThreeD.License`.

{{% /alert %}} 
### **Caricamento di una licenza dal file**
Il modo più semplice per applicare una licenza è inserire il file di licenza nella stessa cartella del file Aspose.3D.dll e specificare solo il nome del file senza un percorso.

{{% alert color="primary" %}} 

Quando si chiama il metodo `SetLicense`, il nome della licenza che si passa dovrebbe essere quello del file di licenza. Ad esempio, se si modifica il nome del file di licenza in "Aspose.3D.lic. xml", passare il nome del file al metodo `threeD.SetLicense(…)`.

{{% /alert %}} 

**Esempio:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**Caricamento di una licenza da un oggetto Stream**
L'esempio seguente mostra come caricare una licenza da un flusso.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **Applica la licenza utilizzando la risorsa incorporata**
Un modo per applicare una licenza è impostarla[Utilizzando un file o un oggetto stream](). Un altro modo accurato per impacchettare la licenza con l'applicazione e assicurarsi che non vada persa è includerla come risorsa incorporata in uno degli assemblaggi che chiama la DLL del componente (inclusa nello Aspose.3D).

Per includere il file di licenza come risorsa incorporata:

1. Nello Visual Studio .NET, includere il file di licenza (.lic) nel progetto selezionando**File**, Allora**Aggiungi elemento esistente**E finalmente**Aggiungi**.
1. Selezionare il file in Solution Explorer.
1. Impostare il**Costruisci azione**A**Risorsa incorporata**Nella finestra Proprietà.
1. Per accedere alla licenza incorporata nell'assembly (come risorsa incorporata), basta aggiungere il file di licenza come risorsa incorporata al progetto e passare il nome del file di licenza al metodo SetLicense. La classe Licenza trova automaticamente il file di licenza nelle risorse incorporate. Non è necessario chiamare i metodi GetExecutingAssembly e GetManifestResourceStream della classe System.Reflection.Assembly nello Microsoft .NET Framework.

Il seguente frammento di codice viene utilizzato per impostare la licenza.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **Applica licenza misurata**
Aspose.3D for .NET API consente agli sviluppatori di applicare una licenza misurata. È un nuovo meccanismo di licenza. Il nuovo meccanismo di licenza sarà utilizzato insieme al metodo di licenza esistente. Quei clienti che desiderano essere fatturati in base all'utilizzo delle funzionalità API possono utilizzare la licenza misurata. Per maggiori dettagli, si prega di fare riferimento a[Domande frequenti sulle licenze misurate](https://purchase.aspose.com/faqs/licensing/metered)Sezione.

È stata aggiunta una nuova classe [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) per applicare la chiave misurata. Questo esempio di codice dimostra come impostare chiavi pubbliche e private con misurazione:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
