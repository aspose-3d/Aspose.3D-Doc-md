---
title: glTF Mesh Features Exempel
type: docs
linkTitle: "glTF-nätverksfunktioner"
description: "Denna dokumentationssida visar hur man skapar en glTF-fil med EXT_mesh_features med Aspose.3D för .NET."
weight: 10
---

# Skapa glTF-filer med EXT_mesh_features

Detta exempel visar hur man skapar en glTF-fil med tillägget EXT_mesh_features med hjälp av Aspose.3D API.

## Kodförklaring

Följande C#-kod skapar en mesh med kontrollpunkter och polygoner, lägger sedan till funktions-ID:n till kontrollpunkterna innan den sparas till en glTF-fil:

```csharp
// Detta exempel skapar en glTF-fil med EXT_mesh_features
// Först skapar vi en mesh
var mesh = new Mesh();

// Lägg till kontrollpunkter (vertices) till meshen
// Den första uppsättningen av fyra punkter skapar en fyrkant i XY-planet på y=1
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // Punkt 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // Punkt 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // Punkt 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // Punkt 3

// Den andra uppsättningen av fyra punkter skapar en annan fyrkant i XY-planet på y=0
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // Punkt 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // Punkt 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // Punkt 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // Punkt 7

// Skapa triangulära ytor (polygoner) från kontrollpunkterna
// Första fyrkanten (punkter 0-3) delas in i två trianglar
mesh.CreatePolygon(0, 1, 2);  // Triangel 0-1-2
mesh.CreatePolygon(0, 2, 3);  // Triangel 0-2-3

// Andra fyrkanten (punkter 4-7) delas också in i två trianglar
mesh.CreatePolygon(4, 5, 6);  // Triangel 4-5-6
mesh.CreatePolygon(4, 6, 7);  // Triangel 4-6-7

// Sedan skapar vi ett användardataelement för att lagra funktions-ID:n
// Detta kommer att associera funktions-ID:n med kontrollpunkterna
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // Elementtyp
    MappingMode.ControlPoint,   // Tillämpa på kontrollpunkter
    ReferenceMode.Direct        // Direkt mappning (inte indexerad)
);

// Tilldela funktions-ID:n till varje kontrollpunkt
// De första fyra punkterna får ID 0, de nästa fyra får ID 1
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// Ange det speciella attributnamnet som följer EXT_mesh_features-specifikationen
// Formatet _FEATURE_ID_<n> känns igen av glTF-exportören
featureId.Name = "_FEATURE_ID_0";

// Spara meshen till en glTF Binary (GLB)-fil
// Exportören kommer automatiskt att generera tilläggsdatan EXT_mesh_features
// Använd en relativ sökväg för utdatafilen
(new Scene(mesh)).Save("mesh_feature.glb");
```

## Viktiga koncept

### Mesh-skapande
- `Mesh`-klassen representerar en polygonmesh-geometri
- Kontrollpunkter definierar vertices av meshen
- `CreatePolygon`-metoden skapar triangulära ytor mellan kontrollpunkter

### Funktions-ID:n
- Funktions-ID:n tillåter gruppering av geometri inom en mesh
- Implementeras genom `VertexElementUserData` med ett speciellt namngivningskonvention
- `_FEATURE_ID_0` indikerar att detta är en funktions-ID-ström
- Flera funktions-ID-strömmar kan skapas med ökande index

### Datatilldelning
- Funktions-ID:n lagras som flyttal
- Varje kontrollpunkt får ett motsvarande funktions-ID-värde
- I detta exempel använder vi två distinkta funktions-ID:n: 0 och 1

### Filexport
- Att spara till GLB-format bevarar alla funktioner inklusive EXT_mesh_features
- Aspose.3D hanterar automatiskt genereringen av tillägget
- Den resulterande filen innehåller metadata om mesh-funktionerna
- Att använda relativa sökvägar gör koden mer portabel och enklare att köra i olika miljöer

Detta exempel visar hur Aspose.3D kan användas för att skapa glTF-filer som använder tillägget EXT_mesh_features för avancerad 3D-datarepresentation.