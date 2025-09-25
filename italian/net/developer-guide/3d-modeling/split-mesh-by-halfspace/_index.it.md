---
title: "Come dividere una mesh per HalfSpace in Aspose.3D"
type: docs
linkTitle: "Split Mesh by HalfSpace"
description: "Impara come dividere mesh 3D usando piani HalfSpace in Aspose.3D"
weight: 10
---

# Divisione di Mesh con HalfSpace in Aspose.3D

Questo tutorial dimostra come utilizzare Aspose.3D per eseguire operazioni di divisione di mesh utilizzando piani HalfSpace. Questa tecnica è utile per estrarre porzioni specifiche di un modello 3D in base a criteri spaziali.

## Comprendere le Operazioni HalfSpace

Un HalfSpace rappresenta uno spazio infinito diviso da un piano. Quando combinato con le operazioni booleane di Aspose.3D, consente di estrarre porzioni specifiche di una mesh che esistono su un lato del piano definito.

### Concetti Chiave:
- **HalfSpace**: Rappresenta uno spazio infinito diviso da un piano
- **Operazioni Booleane**: Utilizzate per estrarre porzioni di mesh relative all'HalfSpace
- **Equazione del Piano**: Definito come ax + by + cz + d = 0, dove (a,b,c) è il vettore normale
- **Lato Positivo**: La porzione di spazio dove il vettore normale del piano punta

## Esempio di Codice: Divisione di una Mesh con HalfSpace

Il seguente codice C# dimostra come creare una semplice mesh a forma di scatola e dividerla utilizzando un piano HalfSpace:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Crea una nuova scena 3D
        Scene scene = new Scene();
        
        // Crea una mesh a forma di scatola (dimensioni 2x2x2 per impostazione predefinita)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // Crea HalfSpace piano di taglio
        HalfSpace halfSpace = new HalfSpace();
        
        // Definisci l'equazione del piano: ax + by + cz + d = 0
        // Utilizzando il vettore normale che punta nella direzione Z
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // Posiziona l'HalfSpace (crea nodo e trasforma)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // Posiziona a z=0.5
        
        // Esegui l'operazione di divisione booleana
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Aggiungi il risultato alla scena e salva
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("Divisione della mesh utilizzando HalfSpace completata con successo.");
    }
}
```

## Spiegazione del Codice

### Requisiti del Namespace
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Contiene le classi HalfSpace e BooleanOperator
using Aspose.ThreeD.Utilities; // Contiene le utility Vector3 e Plane
```

### Creazione della Geometria
1. **Inizializzazione della Scena**: `Scene scene = new Scene();`
2. **Creazione della Scatola**: `(new Box()).ToMesh()` crea un cubo standard
3. **Gerarchia di Nodi**: La mesh viene aggiunta alla scena tramite un nodo figlio

### Definizione del Piano di Taglio
1. **Definizione del Piano**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - Crea un piano XY orizzontale a z=0
   - Il vettore normale (0,0,1) punta verso l'alto

2. **Posizionamento**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Sposta il piano di taglio a z=0.5
   - Influenza quale porzione della mesh viene mantenuta

### Esecuzione dell'Operazione
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Restituisce la porzione di mesh sul lato positivo del piano
- Il risultato viene aggiunto nuovamente alla gerarchia di nodi

### Salvataggio del Risultato
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Formati supportati includono OBJ, STL, FBX, GLTF e altri
- Viene salvata solo la porzione divisa, non la mesh originale

## Visualizzazione dell'Operazione

### Dimensioni Originali della Scatola:
- Si estende da (-1,-1,-1) a (1,1,1)
- Centrata sull'origine

### Con Piano a z=0.5:
- Mantiene la porzione dove z > 0.5 (parte superiore della scatola)
- Scarta la porzione dove z < 0.5 (parte inferiore)

## Utilizzo Avanzato

### Ottenere Entrambi i Lati del Taglio
```csharp
// Divisione originale (lato positivo)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Inverti il piano per il lato negativo
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Regolazione del Piano di Taglio
```csharp
// Orientamento diverso - taglio angolato
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

Questa implementazione dimostra la funzionalità principale delle capacità di divisione della mesh di Aspose.3D utilizzando piani HalfSpace, consentendo l'estrazione precisa della geometria 3D in base a criteri spaziali.