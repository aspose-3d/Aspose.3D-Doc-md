---
title: Hur man kör Aspose.3D i Blazor?
type: docs
weight: 138
url: /sv/net/how-to-run-aspose-3d-in-blazor/
description: Lär dig hur man kör Aspose.3D i Blazor.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Översikt

Blazor is a web application framework developed by Microsoft that allows client-side web applications to be written using C# and .NET. Blazor is distinguished by its use of WebAssembly technology, which enables applications running in the browser to use high-performance native code. Blazor uses a componentized architecture, allowing developers to divide the UI into independent components, thereby achieving code reusability and maintainability. Blazor supports cross-platform development and can run on a variety of modern browsers and devices, including desktop, mobile, and embedded devices.

I allmänhet erbjuder Blazor ett modernt sätt att bygga webbapplikationer, vilket gör det möjligt för utvecklare att bygga högpresterande, interaktiva, och underhållbara webbapplikationer som använder C# och .NET teknologier i webbläsaren.

## Första Blazor-program med Aspose.3D

I detta exempel skapade vi en enkel Blazor server program, skapade en 3d-fil, och tog en skärmdump av filens innehåll och visade den på en webbsida. Under skapandet av projektet kan vi konfigurera det enligt våra behov, såsom att kontrollera alternativet "Aktivera Docker" så att Blazor-applikationen kan byggas och köras i Docker.

### Skapa det första Blazor- programmet

Låt oss använda VS2022-verktyget som exempel för att skapa det första blazor-programmet med Aspose. 3D, följ stegen nedan:
1. Välj Arkiv -> Nytt -> Projekt och filtrera med blazernyckelordet för att välja motsvarande projektmall.
<br>
<img src="1.png" width=80% />
1. Ange projektnamnet till "BlazorTest" och välj sökvägen.
<br>
<img src="2.png" width=80% />
1. Anpassa bibliotek och andra alternativ som används i projektet. Slutligen, klicka på knappen "Skapa" för att generera ditt första blazerprojekt.
<br>
<img src="3.png" width=80% />
1. Efter att ha gått in i projektet, Klicka på "Beroenden" under projektet och välj "Hantera NuGet paket..." för att lägga till Aspose. 3D bibliotek.
<br>
<img src="4.png" width=80% />
1. Skriv in nyckelord för att filtrera och installera det senaste biblioteket Aspose.3D.
<br>
<img src="5.png" width=80% />
1. Dubbelklicka på filen "Index.razor" för att redigera och importera det erforderliga biblioteket. Lägg till några data och bilder.
<br>
<img src="5.png" width=80% />
1. Kompilera och kör projektet, så får du följande resultat.
<br>
<img src="7.png" width=80% />

### Provkod i den första tillämpningen Blazor.

Följande provkod ingår i Index.razor-filen:
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