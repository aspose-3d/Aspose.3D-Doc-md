---
title: Aspose.3D for .NET 2.1.0 Utgivning
type: docs
weight: 40
url: /sv/net/aspose-3d-for-net-2-1-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 2,1,0](https://www.nuget.org/packages/Aspose.3D/2.1.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-196|Separata importalternativ och exportalternativ för alla 3D filformat.|Ny funktion|
|THREEDNET-194|Exportstöd för Collada.|Ny funktion|
|THREEDNET-198|Tillåt användaren att komma åt låg nivå rendering API.|Ny funktion|
|THREEDNET-199|Låt nod uteslutas under export.|Förbättring|
|THREEDNET-195|Visa textur hittades inte på modellen.|Förbättring|
|THREEDNET-203|Tillåt Vector2/Vector3/Vector4/Quaternion att kunna redigeras i fastighetsnätet.|Förbättring|
|THREEDNET-197|Polygon triangulat problem.|FelComment|
|THREEDNET-202|Diffus/Specular/Emissiv fungerar inte om ingen textur används.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se listan för eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till export av Collada-formatet**
Med denna senaste version (2.1.0) kan utvecklare exportera Collada 3D filer. I den föregående versionen (2.0.0), har vi redan lagt till dess importfunktion, eftersom utvecklare också kan konvertera en Collada fil till andra stödda 3D filformat.
### **Lägger till ladda och spara alternativ för 3D Filformat**
Vi har lagt till laddning och spara alternativ för varje filformat. De är omverkade från de ursprungliga IOConfig-underklasserna.
#### **Lägger till Aspose.ThreeD. Format.ColladaSaveOptions/Discreet3DSLoadOptions/Discreet3DSSaveOptions/FBXSaveOtit Uppgifter/LoadOptions/ObjSaveOptions/STLLoadOptions/STLSaveOptions/ U3DLA oadOptions/U3DSaveOptions klass**
1. **ColladaSaveOptions klass**- Den definierar inställningar för att spara en Collada 3D fil.
1. **Diskreet3DSLoadOptions ClassName**- Det definierar inställningar på att ladda en diskret 3DS fil.
1. **Diskret3DSSaveOptions ClassName**- Det definierar inställningar för att spara en diskret 3DS fil.
1. **FBXSaveOptions ClassName**- Den definierar inställningar för att spara en FBX fil.
1. **ObjLoadOptions ClassName**- Det definierar inställningar på att ladda en Obj-fil.
1. **ObjsparaOptions ClassName**- Det definierar inställningar för att spara en Obj-fil.
1. **STLLoadOptions ClassName**- Den definierar inställningar på att ladda en STL-fil.
1. **STLSaveOptions klass**- Den definierar inställningar för att spara en STL fil.
1. **U3DLoadOptions ClassName**- Den definierar inställningar vid lastning av en U3D fil.
1. **U3DSaveaveOptions ClassName**- Det definierar inställningar för att spara en U3D fil.

{{% alert color="primary" %}} 

De gamla IOConfig-underklasserna är markerade föråldrade, de kommer att tas bort i nästa stora version (3.0.0).

{{% /alert %}} 
### **Lägger till metoder till Aspose.ThreeD.Scenklass**
Vi har överbelastat Öppna och Spara metoder i Sceneklassen. Utvecklare kan skicka ett strömobjekt eller direkt filnamn för att importera/exportera en 3D fil med hjälp av de olika laddning/sparande Valmöjligheter.
### **Avlägsnande av FillDummyIndexArray egendom från Aspose.ThreeD.Formats.FBXConfig klass**
Den här egendomen användes inte.
### **Detektera typ av en 3D- fil**
Detektera metoden av Aspose.ThreeD.FileFormat klassen kan känna igen typ av någon stöds 3D fil.
#### **Lägger till detektera, CreateLoadOptions och CreateSaveOptions metoder i Aspose.ThreeD.**
Efter erkännande av en filtyp 3D, Utvecklare kan skapa objekt LoadOptions och SaveOptions med CreateLoadOptions och CreateSaveOptions metoder i filformatklassen.
### **Lägger exkluderade egendom till Aspose.ThreeD.Enhet och Aspose.ThreeD.Node Klasser**
Det gör det möjligt att avlägsna ett företag under exporten.
### **Lägger till Aspose.ThreeD. Render. RenderState Class och Aspose.ThreeD. Render. BlådFactor/ Jämförelse/CullFaceMode/FrontFace/PolygonMode / Stencils**
Renderingstillstånden ger parametrar för GPU att rasterisera trianglar i bildpunkter.

{{% alert color="primary" %}} 

Inkapsling av hårdvara render tillstånd, detaljerad information finns på dokumentation av[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx)[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) och aspx[Vulkan Ordförande](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Lägger till Shader- API:**
Shader-programmen definierar hur trianglarna från världsutrymme ska omvandlas till skärm och beräkna den slutliga pixelfärgen i GPU- sidan ..
#### **Lägger till en abstrakt klass Aspose.ThreeD. Render. SkådareKälla och underklass Aspose.ThreeD. Render.GLSLSource**
GLSSource berättar renderare, källkoden är för OpenGL språk, den kan sammanställas till Aspose.ThreeD. Render. -ShaderProgram.
#### **Lägger till Aspose.ThreeD.Render.ShaderException klass**
Shader relaterade undantag, som huvudsakligen används i shader språket kompilering och länk steget.
#### **Lägger till Aspose.ThreeD.Render.ShaderProgram ClassName**
Det är det kompilerade shaderprogrammet.
#### **Lägg till Aspose.ThreeD.Render.Shadervariabel klass**
Den definierar de variabler som används i shader.
#### **Lägger till en Enumklass Aspose.ThreeD.Render.VariableSemantic**
Det används för att identifiera skuggarvariablens semantiska, Aspose.3D render automatiskt förbereder variabla värden beror på semantik.
### **Lägger till buffertprogrammen**
Buffertarna ger definition och data för trianglarna.
#### **Lägger till ett gränssnitt Aspose.ThreeD.Render.IBuffer**
Det är basgränssnittet för IIndexBuffer och IVertexBuffer.
#### **Lägger till gränssnitt Aspose.ThreeD.Render.IIndexBuffer/IVertexBufferName**
De presenterar maskinvarubuffertar för lagring av geometriindexen.
#### **Lägger till ett enum Aspose.ThreeD.Render.IndexDataTypeName**
Geometriindexens datatyp.
### **Lägger till teckningsprogrammen**
#### **Lägger till ett gränssnitt Aspose.ThreeD.Render.IRenderbar.**
Ett objekt som stöder rendering bör implementera detta gränssnitt.
#### **Lagt till ett enum Aspose.ThreeD.Render.DrawOperation**
Den primitiva typen att rita.
#### **Lägger till ett enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API använder renderingskö för att hantera renderingsarbetsflödet, detta används för att skicka in uppritning till angiven renderingskö.
#### **Lägger till Aspose.ThreeD.Render.RenderResource Class.**
Basklass för att överbrygga Aspose.3D:s modell API till hårdvarresurser, detta används av Aspose.3D internt, men utsätts för att släppa lös full kraft av Aspose.3D rendering.
#### **Lägger till Aspose.ThreeD.Render.RenderableResource Class.**
En underklass av RenderResource, men koncentrera dig på återgivning.
#### **Lägger till Aspose.ThreeD.Entites.ManualEntity Class.**
Användaren bör använda denna klass för att implementera sin egen enhet som stöder rendering, Denna klass inkapslar uppgifter om rendering och resurshantering.
### **Lägger till flera triangulate metoder i Aspose.ThreeD.Enheter.PolygonModifier Class.**
Fler överbelastningar för att förenkla användningen av originalfunktionen.
### **Lägger till CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState och CreateShaderProgram Metoder i Aspose.ThreeD. Render. RenderFactory-klass**
### **Lägger till BindRenderState, Drandexed, Draw och skickar inRenderTask-metoder i Aspose.ThreeD. Render. Hållarklass**
### **Lägger till RenderStage och Shader egenskaper i Aspose.ThreeD.Render.Renderer klass**
