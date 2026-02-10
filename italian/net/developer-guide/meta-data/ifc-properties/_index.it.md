---
description: "Questa pagina di documentazione dimostra come leggere le proprietà da un file IFC utilizzando Aspose.3D per .NET."
linkTitle: "Supporto alle proprietà IFC"
title: "Supporto alle proprietà IFC"
type: docs
weight: 14
---
## Panoramica

Il supporto delle proprietà IFC è una funzionalità di Aspose.3D che consente agli sviluppatori di leggere i set di proprietà e le quantità degli elementi definiti nei file IFC. queste proprietà sono archiviate nelle entità `IFCPROPERTYSET` e `IFCELEMENTQUANTITY` e possono essere accedute tramite il metodo `A3DObject.GetProperty`.

## Cos'è il supporto delle proprietà IFC?

 nello schema IFC, gli elementi costruttivi possono avere set di proprietà associati (`IFCPROPERTYSET`) e quantità degli elementi (`IFCELEMENTQUANTITY`). Aspose.3D mappa questi a un’interfaccia di proprietà generica, esponendoli tramite `A3DObject.GetProperty(string propertyName)`. Questo consente di recuperare valori come la classificazione antincendio, la trasmittanza termica o le quantità dei materiali direttamente dal modello 3D.

## Perché utilizzare il supporto delle proprietà IFC?

* Accedere a dati semantici ricchi senza analizzare manualmente il file IFC.  
* Abilitare processi successivi come la stima dei costi, il controllo di conformità o l’esportazione dei dati.  
* Combinare informazioni geometriche e non geometriche in un unico flusso di lavoro.

## Supporto di Aspose.3D

Il seguente esempio C# dimostra come caricare un file IFC e leggere una proprietà:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Trova un elemento specifico, ad es., una parete
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Recupera il valore di una proprietà
if (wallNode != null)
{
    // Nome della proprietà così come definito nel file IFC
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Esempio di quantità dell'elemento
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Note

* I nomi delle proprietà definiti in un file IFC sono preceduti da `ifc:` per evitare conflitti con le proprietà native.  
* I nomi delle proprietà distinguono tra maiuscole e minuscole e devono corrispondere esattamente a quelli definiti nel file IFC.  
* `GetProperty` restituisce un `object`; è necessario effettuare il cast al tipo appropriato (ad es., `double`, `string`) secondo necessità.  
* Questo esempio di codice dimostra il recupero delle proprietà da `Node`; tuttavia, qualsiasi discendente di `A3DObject` può utilizzare `GetProperty`.  
* Se una proprietà non esiste, `GetProperty` restituisce `null`.

## Riferimenti

* [Link alla documentazione ufficiale di Aspose.3D IFC](/3d/net/supported-file-formats/ifc)  
* Link a [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* Specifica IFC per `IFCPROPERTYSET` e `IFCELEMENTQUANTITY`