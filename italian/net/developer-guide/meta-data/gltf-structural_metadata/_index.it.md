---
title: "Esempio di metadati strutturali glTF"
type: docs
linkTitle: "Metadati strutturali glTF"
description: "Questa pagina della documentazione dimostra come leggere i metadati strutturali da un file glTF utilizzando Aspose.3D for .NET."
weight: 11
---

# Lettura dei metadati strutturali dai file glTF

Questo esempio dimostra come leggere i metadati strutturali da un file glTF che contiene l'estensione EXT_structural_metadata utilizzando l'API Aspose.3D.

## Spiegazione del codice

Il seguente codice C# carica una scena glTF con metadati strutturali, quindi legge e visualizza informazioni sulle tabelle delle proprietà e le loro proprietà:

```csharp
// Carica la scena glTF con EXT_structural_metadata dal file
var scene = Scene.FromFile("ComplexType.gltf");

// Carica i metadati strutturali dalla scena
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("Visualizzazione dei metadati strutturali dal file glTF di input:");

// Itera attraverso tutte le tabelle delle proprietà nei metadati
foreach (var propTable in metadata.PropertyTables)
{
    // Ottiene la classe meta della tabella delle proprietà
    Console.WriteLine($"Tabella delle proprietà {propTable.Name}, nome del tipo : {propTable.MetaClass.Name}");

    // Itera attraverso tutte le proprietà definite nella classe meta
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // Ottiene i dati della proprietà definiti in EXT_structural_metadata
        object property = propTable.Values[propertyDefinition.Name];
        
        // Visualizza il nome, il tipo e il valore della proprietà
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## Concetti chiave

### Metadati strutturali
- La classe `StructuralMetadata` fornisce l'accesso ai metadati definiti nell'estensione EXT_structural_metadata
- Questa estensione permette di memorizzare informazioni semantiche sugli oggetti 3D
- I metadati possono includere tabelle delle proprietà che definiscono attributi per gli oggetti nella scena

### Tabelle delle proprietà
- Rappresentate dalla classe `PropertyTable`
- Ogni tabella ha:
  - Un nome
  - Una classe meta che definisce la struttura
  - Valori che contengono i dati effettivi delle proprietà

### Classi meta
- Definite dalla classe `MetaClass`
- Descrivono la struttura di una tabella delle proprietà
- Contengono una raccolta di definizioni delle proprietà
- Ogni definizione specifica:
  - Nome della proprietà
  - Tipo della proprietà
  - Altri attributi dei metadati

### Accesso alle proprietà
- Le proprietà sono accessibili tramite il dizionario `Values` di una tabella delle proprietà
- La chiave è il nome della proprietà così come definito nella classe meta
- I valori vengono automaticamente convertiti nel tipo appropriato quando possibile

Questo esempio dimostra come Aspose.3D può essere utilizzato per leggere e processare i metadati strutturali dai file glTF, permettendo agli sviluppatori di accedere a informazioni semantiche ricche memorizzate insieme alla geometria 3D.