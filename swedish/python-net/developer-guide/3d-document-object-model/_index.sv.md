---
title: Aspose.3D Dokumentobjektmodell (DOM)
type: docs
weight: 20
url: /sv/python-net/aspose-3d-document-object-model
description: Varje 3Dscen kan omfatta ett antal visningar. Med Aspose.3D for Python via .NET API kan utvecklare fånga en eller flera vyer i en enda skärmbild. De kan göra det i GUI-baserad program eller en bild.
---
Aspose.3D Dokumentobjektmodellen (DOM) är en kraftfull representation av en 3D-scen. Det ger utvecklare möjlighet att läsa, manipulera, och ändra innehållet och formateringen av en 3D scen programmerat.

I det här avsnittet kommer vi att utforska nyckelklasserna i Aspose.3D DOM och deras relationer. Genom att utnyttja dessa klasser kan du få tillgång till olika element inom en 3D scen.

Låt oss ta del i de viktigaste klasserna för Aspose.3D DOM:

* **Scene**: Scenklassen representerar roten i 3D scenhierarkin. Den fungerar som behållare för alla andra element och ger metoder för att manipulera den övergripande scenen.
* **Nod**: Noder är byggstenarna för en 3D scen. De representerar enskilda objekt eller enheter inom scenen, såsom maskor, lampor, kameror eller grupper. Noder kan omvandlas, animeras och struktureras.
* **Enheter**: Enheter klasserna omfattar ett brett utbud av objekt och element som utgör en 3D-scen. Det omfattar enheter som maskor, lampor, kameror, profiler och mer. Dessa entiteter fungerar som byggstenar, så att du kan skapa komplexa scener genom att kombinera och manipulera dem programmerat. Kategorin Enheter ger åtkomst och kontroll över dessa grundläggande element i en 3D scen.
* **Material**: Materialklassen kretsar kring att definiera objektens visuella egenskaper inom en 3D-scen. Den ger verktyg för att programmerat skapa, modifiera och styra material som avgör hur ljuset interagerar med ytor. Genom att justera egenskaper som färg, textur, transparens och reflektion, du kan uppnå olika visuella effekter och anpassa utseendet på dina 3D-modeller.
* **Animeringar**: Animeringsklasserna fokuserar på att skapa och styra rörelser och transformationer inom en 3D-scen. Det gör att du kan programmerat definiera och manipulera animationer, vilket gör det möjligt för objekt att flytta, rotera, skala eller ändra egenskaper över tiden. Med den här kategorin kan du ta med dynamiska och interaktiva element till dina 3D scener.

Genom att använda Aspose. 3D DOM-klasser som nämns ovan, kan du programmerat interagera med och manipulera innehållet och strukturen i en 3D scen. Detta ger flexibilitet och kontroll när du arbetar med 3D-modeller i dina program.


## Scenstruktur

När Aspose. 3D läser en 3D-fil till minnet, det genererar objekt av olika typer för att representera de olika elementen inom 3D scenen.


Scenstrukturen i Aspose.3D följer mönstret sammansatt design, som erbjuder flexibilitet och organisation:

 * Node fungerar som behållare som kan hålla andra noder, vilket gör det möjligt att gruppera olika objekt inom scenen.
 * Varje nod kan ha sin egen transformation, vilket också gäller dess barnnoder.
 * Alla typer av rumsliga enheter i Aspose.3D måste placeras i en nodeinstans. Detta säkerställer att föremål som maskor, lampor, kameror och andra element organiseras inom scenhierarkin.
 * Noder kan innehålla flera material, och förhållandet mellan polygoner och material som är anslutna till en nod är adresserat med `VertexElementMaterial`-konceptet i Mesh-objektet.


![Scene hierarchy](scene.png)


## Rumsliga enheter
Alla rumsliga enheter inom Aspose. 3D ärv från `Entity` klassen, som fungerar som grundläggande byggstenar för att skapa virtuella miljöer. Aspose.3D kategoriserar dessa enheter i flera större kategorier, var och en med sitt eget specifika syfte och funktionalitet.

![Entities](entity.png)

* **Primitivt**Klassen `Primitive` fungerar som basklass för alla procedurmässiga 3D geometrier inom Aspose. 3D, såsom `Cylinder`, `Torus` och `Sphere`. Dessa geometrier kan definieras med hjälp av en minimal uppsättning parametrar, vilket gör det bekvämt att skapa grundläggande 3D former.
* **Geometrin**Geometrier i Aspose. 3D består vanligtvis av hörn, kanter och polygoner som definierar form och struktur för ett 3D objekt. Denna kategori omfattar ett brett utbud av komplexa geometrier som används för att representera olika objekt inom en 3D scen.
* **Profil**: Profiler, liknande primitiva, definiera 2D-slutna konturer i x-y-planet. De ger ett sätt att skapa 2D-former som kan extruderas för att skapa motsvarande 3D- geometrier. Profiler används ofta som utgångspunkt för att skapa mer invecklade 3D objekt.
* **Kurva**: Till skillnad från profiler kan kurvorna vara öppna eller omöjliga. De används för att definiera rumsliga sökvägar i 3D. Kurvor ger ett sätt att skapa flexibla och anpassningsbara sökvägar som objekt kan följa inom en 3D miljö.
* **Extrudering**: Extrusioner är en processuell teknik som används för att konstruera 3D geometrier med hjälp av profiler och kurvor. Genom att tillämpa extrudering på en profil eller en kurva, en 3D form kan genereras genom att utöka profilen eller kurvan längs en angiven riktning. Detta tillvägagångssätt gör det möjligt att skapa mer komplexa och dynamiska geometrier.
* **Frusstump**: Frustum kategorin omfattar föremål som ljus och kameror. Frustums definiera visningsvolymen och perspektivet i en 3D-scen. Kameror använder frustums för att bestämma vilken del av scenen som kommer att vara synlig, medan ljus utnyttjar frustums för att definiera den region inom vilken de belyser scenen.

Dessa större entitetskategorier i Aspose. 3D omfattar en mängd olika enheter som spelar viktiga roller för att bygga och representera virtuella miljöer, tillhandahålla en mångsidig verktygslåda för att skapa och manipulera 3D-scener.


### Geometrityper

![Geometry types](geometries.png)

Aspose.3D contains many geometry types:


* `Mesh` Verktyg för behörighetsbehörighet friendly polygon mesh.
* `PointCloud` Poängmoln.
* `NurbsSurface` Icke-Uniform Rational B-Spline-ytor.
* `Patch` Yta definierat av en uppsättning kontrollpunkter och blandningsfunktioner.
* `TriMesh` Render APIfriendly triangelbaserad mesh.


De viktigaste av dem är `Mesh` och `TriMesh`, skillnaderna är i tabellen:

|Funktion| `Mesh` | `TriMesh` |
| ---     |---     |---        |
|Polygon icke- triangel|JA|Nje|
|Lätt att ändra.|JA|Nje|
|Återanvändning av dataindex|JA|Nje|
|CPU- cache vänligComment|Nje|JA|
|Redigerar API friendly.|Nje|JA|
|Fast layout|Nje|JA|

Klasser som härletts från `Geometry` är designad för ändra och skapande av innehåll medan `TriMesh` är utformad för uppgivning.

Ett `Geometry` består av kontrollpunkter och `VertexElement` som definierar extra data för kontrollpunkt/edge/polygon/polygon vertex, `Geometry` kan innehålla noll eller mer `VertexElement`, beton `Geometry` underklasser implementerade olika metoder för modellering och representerar 3D geometrier.


![Geometry types](mesh.png)


Du kan manuellt skapa ett vertex element och tilldela data för det. Följande kodexempel visar hur man gör detta:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Examples-Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

### Primitiva geometrityper


Aspose. 3D tillhandahåller en uppsättning fördefinierade primitiva geometrityper som följer specifika regler och algoritmer för att skapa 3D modeller. Dessa primitiva typer förenklar processen att skapa 3D geometrier jämfört med att använda mer komplexa geometrityper.

Tillgängliga fördefinierade primitiva typer i Aspose.3D inkluderar:

*  `Box`: The box primitive allows you to create rectangular cuboid shapes defined by their width, height, and depth.
* Cylinder: Med cylindern primitiv kan du generera cylindriska former genom att ange radie och höjd. Detta är användbart för att skapa objekt som rör eller kolumner.
*  `Dish`: The dish primitive enables the creation of dish-shaped geometries, commonly used to represent objects like bowls or satellite dishes.
*  `Plane`: The plane primitive generates flat surfaces defined by their width and length. It is frequently used as a foundation or ground plane in 3D scenes.
*  `Pyramid` Med pyramiden primitiv kan du skapa pyramidformade geometrier som kännetecknas av basstorlek och bashöjd. Detta är användbart för att bygga föremål som byggnader eller pyramider.
*  `Torus` $: Torus primitive kan du skapa munkformade geometrier med angiven radii för de större och mindre cirklarna. Den är lämplig för att skapa föremål som liknar ringar eller däck.
*  `RectangularTorus` $: Den rektangulära torus primitive producerar torusliknande geometrier med rektangulära tvärsnitt istället för cirkulära. Det ger ytterligare flexibilitet för att skapa unika former.
*  `Sphere` $: Sfären primitive genererar perfekt runda geometrier baserat på angiven radie. Detta är användbart för att skapa objekt som planeter eller bollar.

Genom att använda dessa fördefinierade primitiva typer i Aspose. 3D kan du enkelt skapa ett brett utbud av grundläggande 3D geometrier. Detta förenklar modelleringsprocessen och låter dig snabbt forma och montera objekt i dina 3D-scener.

![Primitive geometry types](primitives.png)

Följande kodexempel visar hur man skapar en sfär med angiven radie:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Examples-Working-with-Objects-WorkingWithSphereRadius-WorkingWithSphereRadius.py" >}}

### Extruderingstyper

Extrudering kan användas för att skapa en mängd komplexa 3D-objekt, Det är en grundläggande metod i 3D modellering som innebär att utöka en 2D-profil längs en kurva för att skapa en 3D Objekt.

I Aspose.3D har vi tillhandahållit 3 extruderingstyper:

* `LinearExtrusion` Lineär extrusion tar en 2D-profil som indata och utökar formen i den 3:e dimensionen.
* `RevolvedAreaSolid` Den här klassen representerar en solid modell genom att rotera ett tvärsnitt som tillhandahålls av en profil om en axel.
* `SweptAreaSolid` Den här klassen representerar en solid modell med ett svepande representationsschema som tillåter ett tvärsnitt med 2D-profil att svepa igenom rymden ..


![Extrusions](extrusions.png)

Följande kodexempel visar hur man skapar en linjär extrusion från en textprofil:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Examples-Working-with-LinearExtrusion-Text.py" >}}


### Kurvtyper

I Aspose. 3D, en kurva representerar en eller flera rumsliga sökvägar som kan ta olika former, såsom linjer, NURBS-kurvor, eller sammansatta kurvor bestående av flera kurvsegment. Kurvor används vanligtvis tillsammans med extrusion typer för att skapa dynamiska och intrikata 3D former.

Kurvor kan användas för att definiera komplexa sökvägar som objekt följer inom en 3D-miljö, vilket aktiverar smidiga och exakta rörelser. Genom att använda olika kurvtyper och komponera dem tillsammans, du kan uppnå mångsidiga och anpassningsbara rumsliga sökvägar för dina 3D-modeller.

Dessutom ger vissa filformat som stöds av Aspose.3D möjligheten att importera och exportera kurvadata. Det här låter dig sömlöst integrera kurvor som skapats i externa program eller dela kurvor som genereras inom Aspose. 3D med annan programvara.


![Curve types](curves.png)

## Profiltyper

Aspose. 3D erbjuder ett sortiment av 2D-profiler som kan användas för att skapa stängda former eller konturer inom en 3D-miljö. .. Dessa profiler gör det möjligt att skapa invecklade 2D-strukturer som kan ytterligare extruderas eller manipuleras till 3D geometrier. Här är några anmärkningsvärda profilimplementeringar i Aspose.3D:

* `ParameterizedProfile`: Aspose.3D tillhandahåller flera implementationer som erbjuder profiler med standardformer. Dessa fördefinierade profiler gör det möjligt att snabbt skapa vanliga former som cirklar, rektanglar och polygoner.

* `MirroredProfile`: This profile type allows you to mirror an existing profile along the Y-axis, creating a symmetrical shape. It provides a convenient way to generate balanced and visually appealing profiles.

* `ArbitraryProfile` Med den godtyckliga profilimplementeringen kan du kartlägga en godtycklig kurva för att skapa en stängd profil. Detta ger flexibilitet i att designa anpassade former genom att definiera en kurva och omvandla den till en sluten profil för ytterligare manipulation.

* `Text` $: Aspose.3D inkluderar förmågan att skapa profiler från texten med ett angivet teckensnitt. Denna funktion låter dig skapa profiler i form av bokstäver, siffror eller annat textinnehåll, lägga till ett element av personalisering eller varumärke till dina 3D-modeller.

![2D profile types](profiles.png)

### Kamera och ljustypar

![Camera and light](frustums.png)

## Materialtyper

Aspose. 3D ger stöd till olika typer av material, inklusive Lambert-material, Phong-material, PBR-material, och skuggmaterial (bara tillgängliga i FBX filer).

Varje material i Aspose. 3D kan ha olika egenskaper och egenskaper som definierar dess utseende och beteende inom en 3D scen. Dessa material kan kopplas till textur instanser, förbättra deras visuella egenskaper.

Texturer i Aspose.3D är associerade med ett specifikt materialattribut. Texturtypen kombinerar parameterdefinitionerna för bildkällan och texturprovtagaren. Genom att använda texturer kan du tillämpa detaljerade mönster, färger och andra visuella effekter på ytorna på 3D-modellerna.

Med stöd för en rad materialtyper och möjligheten att ansluta texturer, Aspose. 3D erbjuder flexibilitet när det gäller att skapa visuellt tilltalande och realistiska material för dina 3Dscener.

![Material types](materials.png)

Följande kodexempel visar hur ett PBR-material ska tillämpas på en geometri:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Examples-Geometry-and-Hierarchy-ApplyPBRMaterialToBox-ApplyPBRMaterialToBox.py" >}}

## Animeringsobjekt
Aspose.3D tillhandahåller stöd för animation på datanivå, och beräkningsstöd håller för närvarande på att utvecklas.

I Aspose.3D kan en scen innehålla flera AnimationClip-objekt. Varje animationsklipp kan bestå av flera animationsnoder. Animationsnoden följer det sammansatta designmönstret, vilket gör det möjligt att skapa hierarkiska strukturer med subanimationsnoder.

Animeringsnoder kan associeras med bindpunkter, som definierar egenskaperna för det målobjekt som kommer att animeras. Vektorer är ofta använda datatyper i många enheter egenskaper. Därför kan bindpunkter ha olika animationskanaler för att uppdatera specifika kanaler av vektorn oberoende. Varje kanal innehåller en tangentramsekvens som definierar hur värdet animeras över tiden.

Detta system ger en flexibel ram för att animera objekt i en scen. Genom att definiera animationsklipp, noder, bindpunkter och kanaler, du kan skapa komplexa och dynamiska animationer som påverkar olika egenskaper för enheterna i din 3D-scen.

Med Aspose. 3D stöder för närvarande animation på datanivå, den pågående utvecklingen fokuserar på att utöka beräkningsstödet, som kommer att förbättra möjligheterna att skapa och manipulera animationer inom ramen.

![Animations](animations.png)


En scen med animationer kan ha denna typ av struktur:


![Animations Sample](animation_relations.png)