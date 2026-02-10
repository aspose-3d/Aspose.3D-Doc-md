---
title: Licensing
type: docs
weight: 60
url: /it/java/licensing/
description: Puoi facilmente scaricare/installare Aspose.3D for Java da Aspose repository per la valutazione. Il download della valutazione è lo stesso del download acquistato. La versione di valutazione diventa semplicemente concessa in licenza quando si aggiungono alcune righe di codice per applicare la licenza.
---
##  **Valuta Aspose.3D**
Puoi facilmente scaricare/installare Aspose.3D for Java da [Aspose repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) per la valutazione. Il download della valutazione è lo stesso del download acquistato. La versione di valutazione diventa semplicemente concessa in licenza quando si aggiungono alcune righe di codice per applicare la licenza.

La versione di valutazione fornisce tutte le funzionalità tranne le seguenti:

- Gli utenti possono aprire/importare solo un massimo di 50 3D documenti in una scena.
- Gli utenti possono salvare solo un massimo di 50 3D documenti in una scena.
- Gli utenti vedranno anche una filigrana di valutazione nelle immagini renderizzate e in tutti gli altri file di output.
- Ogni nodo non può avere più di 5 nodi figlio.
- Ogni nodo non può avere più di 2 entità allegate.
- Ogni geometria non può avere più di 2 elementi di vertice collegati.
- Ogni nodo non può avere più di 1 materiale.

{{% alert color="primary" %}} 

Se usi Aspose.3D senza una licenza adeguata, potrebbe essere attivato un**com.aspose.threed.TrialException**Quando l'utilizzo ha raggiunto le restrizioni senza licenza, puoi disattivare l'eccezione:

* [Buy a full featured license](https://purchase.aspose.com/buy).
* Richiedi una licenza temporanea di 30 giorni, fai riferimento a [Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) Per ulteriori informazioni.
.
* Chiama `com.aspose.threed.TrialException.setSuppressTrialException(true)` prima dei tuoi metodi `open`/`save`, i `TrialException` non verranno aumentati durante la chiamata `open`/`save` sulla scena, ma le restrizioni di cui sopra non verranno revocate.
* Usa manualmente un blocco `try/catch` su `Scene.open/save`, questa eccezione è solo una notifica, ignorarla non influirà sul caricamento/salvataggio della scena.

{{% /alert %}} 
##  **Applicazione di una licenza**
La licenza è un file XML di testo normale che contiene dettagli come il nome del prodotto, il numero di sviluppatori a cui è concesso in licenza, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificare il file; anche l'aggiunta involontaria di un'ulteriore interruzione di riga nel file lo invaliderà. È necessario impostare una licenza prima di eseguire qualsiasi operazione con i documenti. Assicurati di farlo prima di creare un oggetto Scene.

Le licenze possono essere applicate da varie località:

- Percorso esplicito
- La cartella che contiene il file JAR di Aspose.3D.
- Una risorsa incorporata nel JAR che si chiama Aspose.3D JAR.

Utilizza il metodo `License.setLicense` per ottenere la licenza delle API. Spesso il modo più semplice per impostare una licenza è inserire il file di licenza nella stessa cartella di Aspose. JAR di 3D e specificare solo il nome del file senza percorso.
###  **Applicare la licenza utilizzando file o oggetto Stream**
In questo esempio Aspose.3D tenterà di trovare il file di licenza nella cartella che contiene i JAR dell'applicazione.

{{< highlight "java" >}}
License license = new License();
license.setLicense("Aspose._3D.lic");
{{< /highlight >}}

Inizializza una licenza da uno stream.

{{< highlight "java" >}}
License license = new License();
try(FileInputStream myStream = new FileInputStream("Aspose._3D.lic")) {
    license.setLicense(myStream);
}
{{< /highlight >}}
###  **Compreso il file di licenza come risorsa incorporata**
Puoi semplicemente copiare il file LIC nella cartella `resources` del tuo progetto. La ricostruzione del progetto dovrebbe incorporare il. Lic file nell'applicazione. File del barattolo. Dopodiché puoi applicare la licenza utilizzando il codice come di seguito:

{{< highlight "java" >}}
License lic = new License();
lic.setLicense(Program.class.getResourceAsStream("Aspose.3D.Java.lic"));
{{< /highlight >}}
###  **Convalidare la licenza**
È possibile convalidare se la licenza è stata impostata correttamente o meno. La classe Licenza ha il campo isLicensed che restituirà true se la licenza è stata impostata correttamente.

{{< highlight "java" >}}
License license = new License();
license.setLicense("Aspose.3D.Java.lic");
    	  
if (License.isLicenseSet()) {
    System.out.println("License is Set!");
}
{{< /highlight >}}
##  **Applica licenza misurata**
Aspose.3D consente agli sviluppatori di applicare la chiave misurata. È un nuovo meccanismo di licenza. Il nuovo meccanismo di licenza sarà utilizzato insieme al metodo di licenza esistente. I clienti che desiderano essere fatturati in base all'utilizzo delle funzionalità API possono utilizzare la licenza misurata. Per maggiori dettagli, fai riferimento alla sezione [Domande frequenti su Licensing misurate](https://purchase.aspose.com/faqs/licensing/metered).

È stata introdotta una nuova classe `Metered` per applicare la chiave misurata. Di seguito è riportato il codice di esempio che mostra come impostare la chiave pubblica e privata misurata.

{{< highlight "java" >}}
// Initialize a Metered license class object
Metered metered = new Metered();
// Set public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
##  **Quando applicare una licenza**
Segui queste semplici regole:

- La licenza deve essere impostata solo una volta per dominio dell'applicazione.
- Devi impostare la licenza prima di utilizzare qualsiasi altro Aspose.3D classi.
- Calling License.SetLicense più volte non è dannoso, ma semplicemente fa perdere tempo al processore.

Se stai sviluppando una libreria di classi, puoi chiamare License.SetLicense da un costruttore statico della tua classe che utilizza Aspose.3D. Il costruttore statico verrà eseguito prima della creazione di un'istanza della classe, assicurandosi che la licenza Aspose.3D sia impostata correttamente.
##  **È possibile modificare il nome del file di licenza**
Il nome del file di licenza non deve essere 'Aspose.3D. LI'. Puoi rinominarlo in qualsiasi cosa ti piaccia e utilizzare quel nome quando chiami License.SetLicense.
##  **Non è possibile trovare il nome del file di licenza Eccezione**
Quando acquisti e scarichi una licenza, il sito web Aspose nomina il file di licenza `Aspose.3D.LIC`. Si scarica il file di licenza utilizzando il browser. Alcuni browser riconoscono il file di licenza come XML e aggiungono un file. Estensione xml ad esso in modo che il nome completo del file sul tuo computer diventi `Aspose.3D.lic.XML`.

Quando Microsoft Windows, ad esempio, è configurato per nascondere le estensioni dei tipi di file noti (purtroppo questo è predefinito nella maggior parte delle installazioni Windows), il file di licenza apparirà come `Aspose.3D.LIC` in Windows Explorer. È probabile che pensi che questo sia il vero nome del file e la licenza di chiamata. SetLicense che lo passa `Aspose.3D.LIC`, ma non esiste un file di questo tipo, da cui l'eccezione.

Per risolvere il problema, rinominare il file per rimuovere l'invisibile. Estensione xml. Ti consigliamo inoltre di disabilitare l'opzione "nascondi estensioni" in Microsoft Windows.

##  **Utilizzo di più API da Aspose**
Se nella tua applicazione utilizzi più API Aspose, ad esempio Aspose.3D e Aspose. Celle, ecco alcuni suggerimenti utili.

- Imposta la licenza per ogni Aspose API separatamente. Anche se hai un singolo file di licenza per tutte le API, ad esempio `Aspose.Total.lic`, devi comunque chiamare `License.setLicense` separatamente per ogni Aspose API che stai utilizzando nella tua applicazione.
- Utilizzare il nome di classe della licenza completamente qualificato. Ogni Aspose API ha una classe di licenza nel suo spazio dei nomi. Ad esempio, Aspose.3D ha `com.aspose.3d.License` e Aspose. Celle ha `com.aspose.cells.License` di classe. L'utilizzo del nome della classe pienamente qualificato consente di evitare qualsiasi confusione su quale licenza viene applicata a quale prodotto.
