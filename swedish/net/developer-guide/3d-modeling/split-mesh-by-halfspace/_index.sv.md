---
title: Hur man delar mesh med halvrum i Aspose.3D
type: docs
linkTitle: Dela upp Mesh med HalfSpace
description: "Lär dig hur du delar 3D-nät för med HalfSpace-plan i Aspose.3D"
weight: 10
---

# Dela Halvrymder i Aspose.3D

Denna handledning visar hur man använder Aspose.3D för att utföra mesh-delningsoperationer med hjälp av halvrumsplan. Denna teknik är användbar för att extrahera specifika delar av en 3D-modell baserat på rumsliga kriterier.

## Förståelse av halvrumsoperationer

Ett halvrum representerar ett oändligt utrymme uppdelat av ett plan. När det kombineras med Aspose.3D:s booleska operationer, tillåter det dig att extrahera specifika delar av en mesh som existerar på ena sidan av det definierade planet.

### Nyckelbegrepp:
- **Halvrum**: Representerar ett oändligt utrymme uppdelat av ett plan
- **Booleska operationer**: Används för att extrahera mesh-delar relativt halvrummet
- **Planekvation**: Definierad som ax + by + cz + d = 0, där (a,b,c) är normalvektorn
- **Positiv sida**: Den delen av rymden där planet normal pekar mot

## Kodexempel: Dela en mesh med halvrum

Denna C#-kod demonstrerar hur man skapar en enkel lådmesh och delar den med ett halvrumsplan:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Skapa en ny 3D-scen
        Scene scene = new Scene();
        
        // Skapa en lådmesh (2x2x2 dimensioner som standard)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // Skapa halvrumsplan för skärning
        HalfSpace halfSpace = new HalfSpace();
        
        // Definiera planekvation: ax + by + cz + d = 0
        // Använda plan normal som pekar i Z-riktning
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // Positionera halvrummet (skapa nod och transformera)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // Position vid z=0.5
        
        // Utför boolesk delningsoperation
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Lägg till resultat i scenen och spara
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("Mesh delning med hjälp av Halvrum slutförd framgångsrikt.");
    }
}
```

## Code Explanation

### Namnrymdskrav
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Innehåller HalfSpace och BooleanOperator klasser
using Aspose.ThreeD.Utilities; // Innehåller Vector3 och Plane verktyg
```

### Skapa geometrin
1. **Sceninitialisering**: `Scene scene = new Scene();`
2. **Låds skapande**: `(new Box()).ToMesh()` skapar en standardkub
3. **Nodhierarki**: Mesh läggs till i scenen genom en barnnod

### Definiera skärningsplanet
1. **Plan definition**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - Skapar ett horisontellt XY-plan vid z=0
   - Normalvektor (0,0,1) pekar uppåt

2. **Positionering**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Flyttar skärningsplanet till z=0.5
   - Påverkar vilken del av meshen som behålls

### Utföra operationen
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Returnerar den delen av meshen på den positiva sidan av planet
- Resultatet läggs tillbaka i nodhierarkin

### Spara resultatet
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Stödda format inkluderar OBJ, STL, FBX, GLTF och mer
- Endast fragmentet som delats sparas, inte den ursprungliga meshen

## Visualisera operationen

### Ursprungliga låddimensioner:
- Spänner från (-1,-1,-1) till (1,1,1)
- Centrerad vid origo

### Med plan vid z=0.5:
- Behåller delen där z > 0.5 (övre delen av lådan)
- Kassera delen där z < 0.5 (nedre delen)

## Avancerad användning

### Få båda sidorna av snittet
```csharp
// Ursprungligt delning (positiv sida)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Invertera plan för negativa sidan
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Justera skärningsplanet
```csharp
// Olika orientering - vinklad skärning
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

Denna implementering demonstrerar kärnfunktionaliteten i Aspose.3D:s mesh-delningsmöjligheter med hjälp av halvrumsplan, vilket möjliggör för exakt extraktion av 3D-geometri baserat på rumsliga kriterier.