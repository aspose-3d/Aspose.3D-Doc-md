---
title: Licenze
description: "Aspose.3D per Python via .NET fornisce diversi piani di acquisto o offre una prova gratuita e una licenza temporanea di 30 giorni per la valutazione utilizzando licenze e politiche di abbonamento."
type: docs
weight: 80
url: /it/python-net/licensing/
---
A volte, per studiare meglio il sistema, vuoi immergerti nel codice il più velocemente possibile. Per rendere questo più facile, Aspose.3D fornisce diversi piani per l'acquisto o offre una prova gratuita e una licenza temporanea di 30 giorni per la valutazione.

{{% alert color="primary" %}}

Tieni presente che ci sono una serie di politiche e pratiche generali che ti guidano su come valutare, concedere correttamente la licenza e acquistare i nostri prodotti. Li puoi trovare nel["Politiche di acquisto e FAQ"](https://purchase.aspose.com/policies)Sezione.

{{% /alert %}}

## **Valuta Aspose.3D**
Puoi facilmente scaricare Aspose.3D per la valutazione. Il pacchetto di valutazione è lo stesso del pacchetto acquistato. La versione di valutazione diventa semplicemente concessa in licenza dopo aver aggiunto alcune righe di codice per applicare la licenza.

## **Limitazione della versione di valutazione**
La versione di valutazione fornisce tutte le funzionalità tranne le seguenti:

- Gli utenti possono aprire/importare solo un massimo di 50 3D documenti su una scena.
- Ogni nodo non può avere più di 5 nodi figlio.
- Ogni nodo non può avere più di 2 entità allegate.
- Ogni geometria non può avere più di 2 elementi di vertice collegati.
- Ogni nodo non può avere più di 1 materiale.
- Gli utenti possono salvare solo un massimo di 50 3D documenti in una scena.
- Gli utenti vedranno anche una filigrana di valutazione nelle immagini renderizzate e in tutti gli altri file di output.

{{% alert color="primary" %}} 
Se stai utilizzando Aspose.3D senza una licenza adeguata, potrebbe scattare un `aspose.threed.TrialException` quando l'utilizzo ha raggiunto le restrizioni senza licenza, puoi disattivare l'eccezione:

* [Acquista una licenza completa in primo piano](https://purchase.aspose.com/buy).
* Richiedi una licenza temporanea di 30 giorni, fai riferimento a [Come ottenere una licenza temporanea?](https://purchase.aspose.com/temporary-license) Per ulteriori informazioni.
* Usa manualmente un blocco 'prova/except' su 'Scene.open/save', questa eccezione è solo una notifica, ignorarla non influirà sul caricamento/salvataggio della scena.

{{% /alert %}} 


## **Informazioni sulla licenza**
Puoi facilmente scaricare una versione di valutazione di Aspose.3D per Python via .NET dal suo[Pagina di download](https://pypi.org/project/aspose.3d/). La versione di valutazione fornisce assolutamente**Le stesse capacità**Come la versione con licenza dello Aspose.3D. Inoltre, la versione di valutazione diventa semplicemente concessa in licenza dopo l'acquisto di una licenza e l'aggiunta di un paio di righe di codice per applicare la licenza.

La licenza è un file XML di testo normale che contiene dettagli come il nome del prodotto, il numero di sviluppatori a cui è concesso in licenza, la data di scadenza dell'abbonamento e così via. Il file è firmato digitalmente, quindi non modificare il file. Anche un'aggiunta involontaria di una interruzione di riga aggiuntiva al contenuto del file lo invaliderà.

Per evitare le limitazioni associate alla versione di valutazione, è necessario impostare una licenza prima di utilizzare**Aspose.3D**. Ti viene richiesto di impostare una licenza solo una volta per domanda o processo.

## Licenza acquistata

Dopo l'acquisto, è necessario applicare il file di licenza o il flusso. Questa sezione descrive le opzioni su come questo può essere fatto e commenta anche alcune domande comuni.

{{% alert color="primary" %}}

È necessario impostare la licenza:
* Solo una volta per dominio dell'applicazione
* Prima di utilizzare qualsiasi altra classe Aspose.3D

{{% /alert %}}

{{% alert color="primary" %}}

Puoi trovare informazioni sui prezzi[“Informazioni sui prezzi”](https://purchase.aspose.com/pricing/3d/family)Pagina.

{{% /alert %}}

### **Impostazione di una licenza nel Aspose.3D per lo Python via .NET**

Le licenze possono essere applicate da varie località:

* Percorso esplicito
* La cartella contenente lo script python che chiama Aspose.3D per Python via .NET
* Stream
* Come una licenza misurata-un nuovo meccanismo di licenza

{{% alert color="primary" %}}

Utilizzare il metodo `set_license` per concedere in licenza un componente.

Chiamare più volte `set_license` non è dannoso, fa solo perdere tempo al processore.

{{% /alert %}}

Nelle sezioni seguenti, descriveremo i due metodi comuni utilizzati per impostare la licenza.

#### **Applicazione di una licenza utilizzando un file**
Il metodo più semplice per impostare una licenza richiede di inserire il file di licenza nella stessa cartella contenente lo script python che chiama Aspose.3D per Python e specificare solo il nome del file senza il suo percorso.

Questo frammento di codice viene utilizzato per impostare un file di licenza:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

Quando si chiama il metodo `set_license`, il nome della licenza deve essere uguale a quello del file di licenza. Ad esempio, è possibile modificare il nome del file di licenza in "Aspose.3D.lica. xml". Quindi, nel tuo codice, devi passare il nuovo nome di licenza (Aspose.3D.lic. xml) al metodo SetLicense.

#### **Applicazione di una licenza da un flusso**
È possibile caricare una licenza da un flusso.

Questo frammento di codice viene utilizzato per applicare una licenza da uno stream:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license(stream)
```

#### Applica licenza misurata

Aspose.3D consente agli sviluppatori di applicare una chiave misurata. Questo è un nuovo meccanismo di licenza.

Il nuovo meccanismo di licenza sarà utilizzato insieme al metodo di licenza esistente. Quei clienti che desiderano essere fatturati in base all'uso delle funzionalità API possono utilizzare le licenze misurate.

Dopo aver completato tutti i passaggi necessari per ottenere questo tipo di licenza, riceverai le chiavi, non il file di licenza. Questa chiave misurata può essere applicata utilizzando la classe `Metered` appositamente introdotta per questo scopo.

Il seguente esempio di codice mostra come impostare chiavi pubbliche e private con misurazione:

```py
import aspose.threed as a3d

# Create an instance of CAD Metered class
metered = a3d.Metered()

# Access the set_metered_key property and pass public and private keys as parameters
metered.set_metered_key("*****", "*****")

# Get metered data amount before calling API
amountbefore = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed Before: " + str(amountbefore))

# Load the scene from disk.
scene = a3d.Scene.from_file("3D Model.fbx")
# Save as pdf
scene.save("out_pdf.pdf", a3d.FileFormat.PDF)

# Get metered data amount After calling API
amountafter = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed After: " + str(amountafter))
```

{{% alert color="primary" %}}

Si prega di notare che è necessario disporre di una connessione Internet stabile per l'uso corretto della licenza misurata, poiché il meccanismo misurato richiede l'interazione costante con i nostri servizi per i calcoli corretti. Per maggiori dettagli, fare riferimento al[“Domande frequenti sulle licenze misurate”](https://purchase.aspose.com/faqs/licensing/metered)Sezione.

{{% /alert %}}



