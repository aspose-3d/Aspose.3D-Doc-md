---
title: Personalizza l'ordine di rotazione nel file FBX
type: docs
weight: 10
url: /it/net/customize-rotation-order-in-fbx-file
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono definire le proprietà native di FBX come RotationOrder.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), a volte, gli sviluppatori richiedono un controllo preciso sulle funzionalità specifiche del formato, come cambiare `RotationOrder` nell'esportatore FBX. Anche se potrebbe non esserci un API pubblico che espone direttamente questa funzionalità, Aspose.3D for .NET fornisce modi per ottenere tali personalizzazioni attraverso la sua architettura flessibile.
{{% /alert %}}



Ecco come puoi gestirlo in Aspose.3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

In questo esempio:

1. Crea una scena da un file RVM.
1. Visita tutti i nodi nella scena.
1. Imposta proprietà personalizzata: il metodo SetProperty viene utilizzato per impostare la proprietà `RotationOrder`, dimostrando come è possibile sfruttare i meccanismi interni per controllare le funzionalità specifiche del formato non direttamente esposte dal pubblico API.
1. Salva la scena: la scena viene salvata con `RotationOrder` personalizzato.

Utilizzando tali tecniche, Aspose.3D consente agli sviluppatori di mettere a punto e controllare le funzionalità specifiche dei formati 3D, assicurando che i requisiti dettagliati e precisi siano soddisfatti in varie applicazioni 3D.