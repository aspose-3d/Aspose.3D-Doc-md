---
title: Licenze
type: docs
weight: 60
url: /it/java/licensing/
description: Puoi facilmente scaricare/installare Aspose.3D for Java dallo Aspose Repository per la valutazione. Il download della valutazione è lo stesso del download acquistato. La versione di valutazione diventa semplicemente concessa in licenza quando si aggiungono alcune righe di codice per applicare la licenza.
---
## **Valuta Aspose.3D**
Puoi facilmente scaricare/installare Aspose.3D for Java da[Aspose Repository](http://repository.aspose.com/repo/com/aspose/aspose-3d/)Per la valutazione. Il download della valutazione è lo stesso del download acquistato. La versione di valutazione diventa semplicemente concessa in licenza quando si aggiungono alcune righe di codice per applicare la licenza.

La versione di valutazione fornisce tutte le funzionalità tranne le seguenti:

- Gli utenti possono aprire/importare solo un massimo di 50 3D documenti su una scena.
- Gli utenti possono salvare solo un massimo di 50 3D documenti in una scena.
- Gli utenti vedranno anche una filigrana di valutazione nelle immagini renderizzate e in tutti gli altri file di output.
- Ogni nodo non può avere più di 5 nodi figlio.
- Ogni nodo non può avere più di 2 entità allegate.
- Ogni geometria non può avere più di 2 elementi di vertice collegati.
- Ogni nodo non può avere più di 1 materiale.

{{% alert color="primary" %}} 

Se stai usando Aspose.3D senza una licenza adeguata, potrebbe scattare un**Com. aspose.threed.TrialException**Quando l'utilizzo ha raggiunto le restrizioni senza licenza, puoi disattivare l'eccezione:

* [Acquista una licenza completa in primo piano](https://purchase.aspose.com/buy).
* Richiedi una licenza temporanea di 30 giorni, fai riferimento a [Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) Per ulteriori informazioni.
.
* Chiama "com.aspose.threed.TrialException.setSuppressTrialException (vero)" prima dei tuoi metodi "open"/"save", la "TrialException" non verrà sollevata durante la chiamata "open"/"save" sulla scena, ma le restrizioni di cui sopra non verranno revocate.
* Usa manualmente un blocco 'prova/cattura' su 'Scene.open/save', questa eccezione è solo una notifica, ignorarla non influirà sul caricamento/salvataggio della scena.

{{% /alert %}} 
## **Applicazione di una licenza**
La licenza è un file XML di testo normale che contiene dettagli come il nome del prodotto, il numero di sviluppatori a cui è concesso in licenza, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificare il file; anche l'aggiunta involontaria di un'ulteriore interruzione di riga nel file lo invaliderà. È necessario impostare una licenza prima di eseguire qualsiasi operazione con i documenti. Assicurati di farlo prima di creare un oggetto Scene.

Le licenze possono essere applicate da varie località:

- Percorso esplicito
- La cartella che contiene il file JAR dello Aspose.3D.
- Una risorsa incorporata nel JAR chiamata Aspose.3D JAR.

Utilizzare il metodo `License.setLicense` per concedere in licenza le API. Spesso il modo più semplice per impostare una licenza è inserire il file di licenza nella stessa cartella del JAR dello Aspose.3D e specificare solo il nome del file senza percorso.
### **Applicare la licenza utilizzando file o oggetto Stream**
In questo esempio Aspose.3D tenterà di trovare il file di licenza nella cartella che contiene i JAR dell'applicazione.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingFile.java" >}}

Inizializza una licenza da uno stream.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingStreamObject.java" >}}
### **Compreso il file di licenza come risorsa incorporata**
Puoi semplicemente copiare il file LIC nella cartella `resources` del tuo progetto. La ricostruzione del progetto dovrebbe incorporare il. Lic file nell'applicazione. File del barattolo. Dopodiché puoi applicare la licenza utilizzando il codice come di seguito:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-FileAsEmbeddedResource.java" >}}
### **Convalidare la licenza**
È possibile convalidare se la licenza è stata impostata correttamente o meno. La classe Licenza ha il campo isLicensed che restituirà true se la licenza è stata impostata correttamente.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ValidateLicense.java" >}}
## **Applica licenza misurata**
Aspose.3D consente agli sviluppatori di applicare la chiave misurata. È un nuovo meccanismo di licenza. Il nuovo meccanismo di licenza sarà utilizzato insieme al metodo di licenza esistente. Quei clienti che desiderano essere fatturati in base all'utilizzo delle funzionalità API possono utilizzare la licenza misurata. Per maggiori dettagli, si prega di fare riferimento a[Domande frequenti sulle licenze misurate](https://purchase.aspose.com/faqs/licensing/metered)Sezione.

È stata introdotta una nuova classe `Metered` per applicare la chiave misurata. Di seguito è riportato il codice di esempio che mostra come impostare la chiave pubblica e privata misurata.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-PublicAndPrivateKeys.java" >}}
## **Quando applicare una licenza**
Segui queste semplici regole:

- La licenza deve essere impostata solo una volta per dominio dell'applicazione.
- È necessario impostare la licenza prima di utilizzare qualsiasi altra classe Aspose.3D.
- Calling License.SetLicense più volte non è dannoso, ma semplicemente fa perdere tempo al processore.

Se stai sviluppando una libreria di classi, puoi chiamare License.SetLicense da un costruttore statico della tua classe che utilizza Aspose.3D. Il costruttore statico verrà eseguito prima che venga creata un'istanza della classe, assicurandosi che la licenza Aspose.3D sia impostata correttamente.
## **È possibile modificare il nome del file di licenza**
Il nome del file di licenza non deve essere 'Aspose.3D.LIC'. Puoi rinominarlo in qualsiasi cosa ti piaccia e utilizzare quel nome quando chiami License.SetLicense.
## **Non è possibile trovare il nome del file di licenza Eccezione**
Quando si acquista e si scarica una licenza, il sito web Aspose nomina il file di licenza `Aspose.3D.LIC`. Si scarica il file di licenza utilizzando il browser. Alcuni browser riconoscono il file di licenza come XML e aggiungono un file. Estensione xml ad esso in modo che il nome completo del file sul computer diventa `Aspose.3D.lic.XML`.

Quando Microsoft Windows, ad esempio, è configurato per nascondere le estensioni dei tipi di file noti (purtroppo questo è predefinito nella maggior parte delle installazioni Windows), il file di licenza apparirà come `Aspose.3D.LIC` in Windows Explorer. È probabile che si pensi che questo sia il vero nome del file e chiamare la licenza. SetLicense che lo passa `Aspose.3D.LIC`, ma non esiste un tale file, quindi l'eccezione.

Per risolvere il problema, rinominare il file per rimuovere l'invisibile. Estensione xml. Ti consigliamo inoltre di disabilitare l'opzione "nascondere le estensioni" in Microsoft Windows.

## **Utilizzo di più API da Aspose**
Se nell'applicazione si utilizzano più API Aspose, ad esempio Aspose.3D e Aspose.Cells, ecco alcuni suggerimenti utili.

- Impostare separatamente la licenza per ogni Aspose API. Anche se si dispone di un singolo file di licenza per tutte le API, ad esempio `Aspose.Total.lic`, è comunque necessario chiamare lo `License.setLicense` separatamente per ogni Aspose API che si sta utilizzando nell'applicazione.
- Utilizzare il nome di classe della licenza completamente qualificato. Ogni Aspose API ha una classe di licenza nel suo spazio dei nomi. Ad esempio, Aspose.3D ha `com.aspose.3d.License` e Aspose.Cells ha classe `com.aspose.cells.License`. L'utilizzo del nome della classe pienamente qualificato consente di evitare qualsiasi confusione su quale licenza viene applicata a quale prodotto.
