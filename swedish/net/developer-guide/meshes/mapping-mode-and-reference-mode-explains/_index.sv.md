---
title: MappingMode och ReferenceMode explains
type: docs
weight: 10
url: /sv/net/mapping-mode-and-reference-mode-explains
description: Använder Aspose. 3D for .NET, kan utvecklare definiera mesh med olika vertexdataelement, Här förklarar vi hur man kartlägger data till meshes komponent och resuze data.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET](https://products.aspose.com/3d/net/) kan utvecklare definiera maskor med olika vertexdataelement, inklusive normala, färger och vikter. Aspose.3D erbjuder två mekanismer för att optimera återanvändning av data: `MappingMode` och `ReferenceMode`. Dessa mekanismer är utformade för att minimera maskornas minnesfotavtryck. särskilt i avancerade format som FBX och USD. MappingMode möjliggör effektiv kartläggning av vertex-data till mesh-komponenter, medan ReferenceMode underlättar referensen av vertex elementdata över flera mesh-komponenter. Tillsammans, dessa funktioner förbättra prestanda och minneseffektivitet, vilket gör Aspose. 3D ett kraftfullt verktyg för hantering av komplexa 3D-modeller i .NET-program.

{{% /alert %}}



###  `MappingMode` förklarar

 `MappingMode` Bestämmer hur elementdata mappas till geometrins yta i Aspose.3D for .NET. Den ger olika sätt att definiera denna kartläggning:

1. **Kontrollpunkter**, Varje dataelement är mappad till styrpunkten av geometrin. Detta läge säkerställer att varje styrpunkt, som definierar geometrins form, associeras med ett specifikt dataelement.
1. **PolygonVertex**, Uppgifterna är mappad till vertex av en polygon. I de fall där en styrpunkt delas med flera polygoner, varje instans av styrpunkten, som den förekommer i olika polygoner, kommer att ha sina egna tydliga uppgifter. Detta säkerställer att även delade styrpunkter kan ha unika data när de fungerar som hörn för olika polygoner.
1. **PolygonName**, Uppgifterna är mappad till hela polygonen. Detta innebär att alla hörn i en polygon delar samma dataelement. Detta läge är användbart när enhetliga data behöver användas över hela polygonytan, vilket säkerställer konsistens inom polygonen.
1. **Kant**, Uppgifterna kartläggs till kanterna av geometrin. Varje endpoint för en kant delar samma data, vilket ger ett sätt att applicera enhetliga data till kanterna samtidigt som det tillåter olika data för olika kanter. Detta kan vara särskilt användbart för att definiera egenskaper som är specifika för kanter, t.ex. stigningsvärden eller kantbaserade egenskaper
1. **Allt samma**, En enda dataelement är kartlagt till hela ytan av geometrin. Oavsett om data tolkas som kontrollpunkter, polygon hörn eller kanter, Samma datavärde tillämpas jämnt för alla delar. Detta läge är idealiskt för scenarier där ett konstant värde måste upprätthållas under hela geometrin. säkerställer en enhetlig attribut i hela modellen 3D.




###  `ReferenceMode` förklarar
 `ReferenceMode` definierar om data ska återanvändas enligt index, det finns tre regler för `ReferenceMode`:

1.1**Direkta**, Refereras data direkt, och lagras i `VertexElement`'s `Data` egendom.
1.1**IndexToDirectComment**, Hänvisas uppgifterna med index, och därefter åtkomnas genom index i `VertexElement`.
1.1**Index**, Är data endast refererade med index, nu bara `VertexElementMaterial` använder detta referensläge, Detta liknar `IndexToDirect` men skillnaderna är att materialen definieras under `Node`s egenskap `Materials`, inte i `VertexElementMaterial`, alla `VertexElement` fungerar bara med primitiv data.



Till exempel, med en definition av en kub:

{{< highlight "csharp" >}}
var cube = new Mesh();
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};
cube.ControlPoints.AddRange(controlPoints);

// Front face (Z+)
cube.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
cube.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
cube.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
cube.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
cube.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
cube.CreatePolygon(new int[] { 3, 2, 6, 7 });

var vertexColor = (VertexElementVertexColor) cube.CreateElement(VertexElementType.VertexColor);
vertexColor.MappingMode = MappingMode.ControlPoint;
var red = new Vector4(1, 0, 0, 1);
var green = new Vector4(0, 1, 0, 1);
var blue = new Vector4(0, 0, 1, 1);
var white = new Vector4(1, 1, 1, 1);

{{< /highlight >}}

Om du vill tilldela rött till kontrollpunkterna 0 och 1, grönt till kontrollpunkterna 2 och 3, blått för att kontrollera punkterna 4 och 5, och vitt till Kontrollpunkterna 6 och 7, kan du uppnå detta med följande tillvägagångssätt:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.Direct;
vertexColor.Data.Add(red); // 0
vertexColor.Data.Add(red); // 1
vertexColor.Data.Add(green); // 2
vertexColor.Data.Add(green); // 3
vertexColor.Data.Add(blue); // 4
vertexColor.Data.Add(blue); // 5
vertexColor.Data.Add(white); // 6
vertexColor.Data.Add(white); // 7
{{< /highlight >}}

För att tilldela färger för att styra punkter effektivt och minska minnesförbrukningen, kan du använda index för att referera färgerna. Genom att definiera färgerna separat och sedan hänvisa dem med index, kan du minimera redundans. Så här kan du uppnå detta:

Först, definiera 4 färger i Vector4 typ för de unika färgerna, och sedan använda en serie av 8 index för att tilldela dessa färger till varje kontrollpunkt:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

I detta tillvägagångssätt:

1. Definiera unika färger: Endast 4 färger definieras (röd, grön, blå, vit) som Vector4.
1. Skapa en färgindex matris: En matris med 8 index används för att referera dessa 4 färger för varje kontrollpunkt.
1. Karta färger med index: Genom att referera färgerna genom index, reducerar du minnesförbrukningen, eftersom varje färg lagras en gång och återanvänds över flera styrpunkter.

Den här metoden optimerar minnesanvändningen genom att minska redundant datalagring, vilket gör din 3D-modell effektivare.