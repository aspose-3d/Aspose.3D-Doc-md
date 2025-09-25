---
title: Esempio di funzionalità della mesh glTF
type: docs
linkTitle: Caratteristiche della Mesh glTF
description: Questa pagina di documentazione dimostra come creare un file glTF con EXT_mesh_features utilizzando Aspose.3D per .NET.
weight: 10
---

# Creazione di file glTF con EXT_mesh_features

Questo esempio dimostra come creare un file glTF con l'estensione EXT_mesh_features utilizzando l'API Aspose.3D.

## Spiegazione del codice

Il seguente codice C# crea una mesh con punti di controllo e poligoni, quindi aggiunge ID delle caratteristiche ai punti di controllo prima di salvare in un file glTF:

```csharp
// Questo esempio creerà un file glTF con EXT_mesh_features
// Prima creiamo una mesh
var mesh = new Mesh();

// Aggiungi punti di controllo (vertici) alla mesh
// Il primo set di quattro punti crea un quadrato nel piano XY a y=1
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // Punto 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // Punto 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // Punto 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // Punto 3

// Il secondo set di quattro punti crea un altro quadrato nel piano XY a y=0
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // Punto 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // Punto 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // Punto 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // Punto 7

// Crea facce triangolari (poligoni) dai punti di controllo
// Il primo quadrato (punti 0-3) è diviso in due triangoli
mesh.CreatePolygon(0, 1, 2);  // Triangolo 0-1-2
mesh.CreatePolygon(0, 2, 3);  // Triangolo 0-2-3

// Il secondo quadrato (punti 4-7) è anch'esso diviso in due triangoli
mesh.CreatePolygon(4, 5, 6);  // Triangolo 4-5-6
mesh.CreatePolygon(4, 6, 7);  // Triangolo 4-6-7

// Quindi creiamo un elemento dati utente per memorizzare gli ID delle caratteristiche
// Questo assocerà gli ID delle caratteristiche ai punti di controllo
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // Tipo di elemento
    MappingMode.ControlPoint,   // Applica ai punti di controllo
    ReferenceMode.Direct        // Mappatura diretta (non indicizzata)
);

// Assegna ID delle caratteristiche a ciascun punto di controllo
// I primi quattro punti ottengono l'ID 0, i successivi quattro ottengono l'ID 1
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// Imposta il nome dell'attributo speciale che conforme alla specifica EXT_mesh_features
// Il formato _FEATURE_ID_<n> è riconosciuto dall'esportatore glTF
featureId.Name = "_FEATURE_ID_0";

// Salva la mesh in un file glTF Binary (GLB)
// L'esportatore genererà automaticamente i dati dell'estensione EXT_mesh_features
// Utilizza un percorso relativo per il file di output
(new Scene(mesh)).Save("mesh_feature.glb");
```

## Concetti chiave

### Creazione della mesh
- La classe `Mesh` rappresenta una geometria mesh poligonale
- I punti di controllo definiscono i vertici della mesh
- Il metodo `CreatePolygon` crea facce triangolari tra i punti di controllo

### ID delle caratteristiche
- Gli ID delle caratteristiche consentono di raggruppare la geometria all'interno di una mesh
- Implementati tramite `VertexElementUserData` con una convenzione di denominazione speciale
- `_FEATURE_ID_0` indica che questo è un flusso di ID delle caratteristiche
- È possibile creare più flussi di ID delle caratteristiche con indici crescenti

### Assegnazione dei dati
- Gli ID delle caratteristiche sono memorizzati come valori float
- Ogni punto di controllo ottiene un valore ID delle caratteristiche corrispondente
- In questo esempio, utilizziamo due ID delle caratteristiche distinti: 0 e 1

### Esportazione dei file
- Il salvataggio in formato GLB preserva tutte le funzionalità, inclusa EXT_mesh_features
- Aspose.3D gestisce automaticamente la generazione dell'estensione
- Il file risultante contiene metadati sulle caratteristiche della mesh
- L'utilizzo di percorsi relativi rende il codice più portatile e più facile da eseguire in diversi ambienti