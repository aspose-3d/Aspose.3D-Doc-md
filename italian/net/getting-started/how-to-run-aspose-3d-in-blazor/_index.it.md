---
title: Come eseguire Aspose.3D in Blazor
type: docs
weight: 138
url: /it/net/how-to-run-aspose-3d-in-blazor/
description: Scopri come eseguire Aspose.3D in Blazor.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Panoramica

Blazor è un framework di applicazioni web sviluppato da Microsoft che consente di scrivere applicazioni web lato client utilizzando C# e .NET. Blazor si distingue per il suo utilizzo della tecnologia WebAssembly, che consente alle applicazioni in esecuzione nel browser di utilizzare codice nativo ad alte prestazioni. Blazor utilizza un'architettura composta, consentendo agli sviluppatori di dividere l'interfaccia utente in componenti indipendenti, ottenendo così la riusabilità e la manutenibilità del codice. Blazor supporta lo sviluppo multipiattaforma e può essere eseguito su una varietà di browser e dispositivi moderni, inclusi dispositivi desktop, mobili e incorporati.

In generale, Blazor fornisce un modo moderno per creare applicazioni web, consentendo agli sviluppatori di creare applicazioni web ad alte prestazioni, interattive e manutenibili utilizzando le tecnologie C# e .NET nel browser.

## Prima applicazione Blazor con Aspose.3D

In questo esempio, abbiamo creato una semplice applicazione server Blazor, creato un file 3d e abbiamo preso uno screenshot del contenuto del file e lo abbiamo visualizzato su una pagina web. Durante il processo di creazione del progetto, possiamo configurarlo in base alle nostre esigenze, come controllare l'opzione "Abilita Docker" in modo che l'applicazione Blazor possa essere creata ed eseguita in Docker.

### Creare la prima applicazione Blazor

Utilizziamo lo strumento VS2022 come esempio per creare la prima applicazione blazor con Aspose.3D, segui i passaggi seguenti:
1. Selezionare File -> Nuovo-> Progetto e filtrare utilizzando la parola chiave blazer per selezionare il modello di progetto corrispondente.
<br>
<img src="1.png" width=80% />
1. Impostare il nome del progetto su "BlazorTest" e selezionare il percorso.
<br>
<img src="2.png" width=80% />
1. Configura le librerie e le altre opzioni utilizzate nel progetto. Infine, fai clic sul pulsante "Crea" per generare il tuo primo progetto di blazer.
<br>
<img src="3.png" width=80% />
1. Dopo aver inserito il progetto, fai clic su "Dipendenze" nel progetto e seleziona "Gestisci NuGet pacchetti..." per aggiungere la libreria Aspose.3D.
<br>
<img src="4.png" width=80% />
1. Inserisci le parole chiave per il filtraggio e installa l'ultima libreria Aspose.3D.
<br>
<img src="5.png" width=80% />
1. Fare doppio clic sul file "Index.razor" per modificare e importare la libreria richiesta. Aggiungi alcuni dati e immagini.
<br>
<img src="5.png" width=80% />
1. Compila ed esegui il progetto e otterrai i seguenti risultati.
<br>
<img src="7.png" width=80% />

### Codice campione nella prima applicazione Blazor

Il seguente codice di esempio è incluso nel file Index.razor:
```
@page "/"
@using Aspose.ThreeD;
@using Aspose.ThreeD.Entities;
@using Aspose.ThreeD.Utilities;

<PageTitle>Index</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<SurveyPrompt Title="How is Blazor working for you?" />

<img src="@imageUrl" />

@code
{
    private string imageUrl="https://docs.aspose.com/3d/net/working-with-cylinder/working-with-cylinder_1.png";

    public Index()
    {
        CreateFile();
    }

    private void CreateFile()
    {
        // Create a scene
        Scene scene = new Scene();

        // Initialize cylinder
        var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

        // Set OffsetTop
        cylinder1.OffsetTop = new Vector3(5, 3, 0);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

        // Intialze second cylinder without customized OffsetTop
        var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder2);

        // Save
        scene.Save("CustomizedOffsetTopCylinder.obj");
    }
}

```