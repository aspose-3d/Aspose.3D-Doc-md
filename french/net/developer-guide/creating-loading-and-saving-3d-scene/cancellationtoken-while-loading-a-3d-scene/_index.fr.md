---
title: CancellationToken lors du chargement d'une scène 3D dans C#
linktitle: CancellationToken lors du chargement d'une scène 3D
type: docs
weight: 80
url: /fr/net/cancellationtoken-while-loading-a-3d-scene/
description: Vous pouvez utiliser CancellationTokenSource pour annuler la tâche enregistrer/ouvrir à tout moment avec C# 3D manipulation de fichier et conversion API.
---
##  **CancellationToken lors du chargement d'une scène 3D**
Toutes les méthodes d'ouverture/de sauvegarde auront un paramètre d'annulation supplémentaire Token avec une valeur par défaut, de sorte que les codes qui ont utilisé ces méthodes n'ont pas besoin de modifier pour compiler.

Vous pouvez utiliser `CancellationTokenSource` pour annuler la tâche de sauvegarde/ouverture à tout moment, comme indiqué dans cet exemple de code C# avec la manipulation des formats de fichier C# 3D API:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
