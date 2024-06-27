---
title: Comment exécuter Aspose.3D dans Blazor
type: docs
weight: 138
url: /fr/net/how-to-run-aspose-3d-in-blazor/
description: Apprenez à exécuter Aspose.3D dans Blazor.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Aperçu

Blazor est un framework d'application web développé par Microsoft qui permet d'écrire des applications web côté client en utilisant C# et .NET. Blazor se distingue par son utilisation de la technologie WebAssembly, qui permet aux applications exécutées dans le navigateur d'utiliser du code natif haute performance. Blazor utilise une architecture componentized, permettant aux développeurs de diviser l'interface en composants indépendants, réalisant ainsi la réutilisabilité et la maintenabilité du code. Blazor prend en charge le développement multiplateforme et peut fonctionner sur une variété de navigateurs et d'appareils modernes, y compris les appareils de bureau, mobiles et intégrés.

En général, Blazor fournit un moyen moderne de créer des applications Web, permettant aux développeurs de créer des applications Web haute performance, interactives et maintenables en utilisant les technologies C# et .NET dans le navigateur.

## Première application Blazor avec Aspose.3D

Dans cet exemple, nous avons créé une simple application de serveur Blazor, créé un fichier 3D, et pris une capture d'écran du contenu du fichier et affiché sur une page Web. Pendant le processus de création du projet, nous pouvons le configurer en fonction de nos besoins, comme cocher l'option "Activer Docker" afin que l'application Blazor puisse être construite et exécutée dans Docker.

### Créer la première application Blazor

Utilisons l'outil VS2022 comme exemple pour créer la première application blazor avec Aspose.3D, suivez les étapes ci-dessous:
1. Sélectionnez Fichier-> Nouveau-> Projet et filtrez à l'aide du mot clé blazer pour sélectionner le modèle de projet correspondant.
<br>
<img src="1.png" width=80% />
1. Définissez le nom du projet sur "BlazorTest" et sélectionnez le chemin.
<br>
<img src="2.png" width=80% />
1. Configurez les bibliothèques et les autres options utilisées dans le projet. Enfin, cliquez sur le bouton "Créer" pour générer votre premier projet de blazer.
<br>
<img src="3.png" width=80% />
1. Après avoir entré le projet, cliquez sur "Dépendances" sous le projet et sélectionnez "Gérer NuGet Packages..." pour ajouter la bibliothèque Aspose.3D.
<br>
<img src="4.png" width=80% />
1. Entrez les mots-clés pour filtrer et installez la dernière bibliothèque Aspose.3D.
<br>
<img src="5.png" width=80% />
1. Double-cliquez sur le fichier "Index.razor" pour modifier et importer la bibliothèque requise. Ajoutez des données et des images.
<br>
<img src="5.png" width=80% />
1. Compilez et exécutez le projet, et vous obtiendrez les résultats suivants.
<br>
<img src="7.png" width=80% />

### Exemple de code dans la première application Blazor

L'exemple de code suivant est inclus dans le fichier Index.razor:
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