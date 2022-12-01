---
title: Aspose.3D for .NET 2,0,0 Utgivning
type: docs
weight: 50
url: /sv/net/aspose-3d-for-net-2-0-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 2,0](https://www.nuget.org/packages/Aspose.3D/2.0.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-113|Importstöd för Collada|Ny funktion|
|THREEDNET-183|Effekter efter bearbetning|Ny funktion|
|THREEDNET-191|Använd Vector4 för att representera UV-koordinater.|Förbättring|
|THREEDNET-189|Render kan krascha programmet på 64bits plattform.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se listan för eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Realtidsgivning**
Det gör det möjligt för utvecklare att utföra högpresterande realtids rendering på ett GUI ramverk som WinForms, det är ramverket oberoende, så de andra GUI-ramverken bör också stödja detta.
#### **Lägger till Collada format**
I denna version (2.0.0), utvecklare kan importera Collada 3D filer, så Collada fastighet läggs till i Aspose.ThreeD. Filformatklass
#### **Lägger till Aspose.ThreeD.Utiliteter.BoundingBox och Aspose.ThreeD.Utilities.BoundingBoxExtent klasser**
De BoundingBox och BoundingBoxExtent klasserna representerar avgränsande ruta av en 3D nod. Utvecklare kan återställa kameran och beräkna höjden från avgränsande ruta. Den oändliga eller noll avgränsande lådan innebär att scenen inte har några geometrier och bara justera kamerans höjd när den är ändlig.
#### **Typ om namn Aspose.ThreeD.UpVector till Aspose.ThreeD.Axis.**
UppVector klassen har döpts om till Axis klass.
#### **Lägger till Aspose.ThreeD.Render.DriverException klass**
Undantagen för den interna renderaren lindas in som DriverException.
#### **Lägger till Aspose.ThreeD.Render.InitializationException klass**
Detta undantag kastas medan renderingen inte initieras, till exempel att initiera den på en dator som inte har någon hårdvaruporter på OpenGL 4.0.
#### **Lägger till Aspose.ThreeD.Render.Renderer klass**
Skapa ett Renderer-objekt och visa fönster från fönstrets infödda handtag. Just nu stöder vi bara infödda fönsterhandtag från Microsoft Windows. Vi kommer att stödja fler plattformar i framtiden. CreateRenderer metod i Renderer klassen skapar en hårdvara OpenGL-backend renderare och vissa interna initieringar kommer att göra e. När återgivaren går utanför räckvidden kommer även de ohanterade hårdvararesurserna att bortskaffas.
#### **Lägger till Aspose.ThreeD.Render.Viewport klass**
Aspose.3D API stöder tre typer av visningsplatser. Sedan målet renderar varje visning av dessa typer.
#### **Lägger till Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow klass**
- IRenderTarget är basgränssnittet för IRenderTexture/IRenderWindow.
- IRenderTexture gör det möjligt att göra scenen till en eller flera texturer (texturer finns i videominnet och kan överföras till systemminnet )
- IRenderWindow tillåter att göra scenen till fönster i realtid.
#### **Lägger till Aspose.ThreeD.Render.ITextureUnit och Aspose.ThreeD.Render.TextureType klasser**
ITextureUnit är faktiskt texturprovtagaren i GPU-sidan och texturdata i CPU- eller GPU-minnet.
#### **Lägger till Aspose.ThreeD.Render.PostProcessing klass**
PostProcessing klass tillåter utvecklare att använda realtidsfilter för bildbearbetning på den återgivna bilden. I denna version har vi tillhandahållit 4 inbyggda efterbehandlingseffekter. Vi tillåter utvecklare att ha en egen egna efterbehandlingsalgoritm i den framtida versionen.
#### **Lägger till Aspose.ThreeD.Render.RenderFaktorklass**
Det hjälper i att göra en scen till texturer eller fönster i realtid.
#### **Lägger till Aspose.ThreeD.Render.RenderParameters klass**
Den definierar parametrarna om hur man skapar renderingen mål som färg bitar, djup bitar, stencil bitar, dubbel buffert.
#### **AddData metoder läggs till Aspose.ThreeD.Enheter.VertexElementUV klass**
VertexElementUV:s basklass har ändrats från VertexElementTemplate<Vector2>Till VertexElementTemplate<Vector4>, Det kommer bara att lagra Vector4 sedan 2.0.0, så två hjälpmedel metoder lades till för att användaren kunde lägga till en lista över Vector2 och Vector3 till VertexElementUV, det kommer att internt expandera Vector2/Vector3 till Vector4 och lämna restens fält noll:
#### **Fastighetsförändringar i klass Aspose.ThreeD.FileFormatt**
Egenskaperna FileFormat ändras från heltal till System.Version.
#### **GetBoundingBox metod läggs till Aspose.ThreeD.Node**
Det gör det möjligt för utvecklare att få axel-aligned avgränsande ruta.
