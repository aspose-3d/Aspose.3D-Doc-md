---
title: Aspose.3D for .NET 1.3.0 Utgivning
type: docs
weight: 100
url: /sv/net/aspose-3d-for-net-1-3-0-release-notes/
---
## **Andra förbättringar och förändringar**

|**Nyckel** |**Sammanfattning** |**Kategori** |
|:- |:- |:- |
|THREEDNET-127 |Lässtöd av Universal 3D format.|Ny funktion|
|THREEDNET-133 |Verifiera Aspose.3D namnrymder överensstämmer med Microsoft riktlinjer.|Förbättring|
|THREEDNET-130 |Fix Aspose licensmissbruk fråga kan orsakas av Aspose Ventures.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se listan för eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Namnrymd och klassnamn ändringar:**
- Namnrymden Aspose.ThreeD.Animationer ändrade till Aspose.ThreeD.Animation
- Klass Aspose.ThreeD.Animationer.Animation ändrad till Aspose.ThreeD.AnimationNod
- Namnrymd Aspose.ThreeD.IO ändrad till Aspose.ThreeD.Formats
- Namnrymden Aspose.ThreeD.Användningar ändras till Aspose.ThreeD.Användningar
#### **Funktionella ändringar:**
- Lagt till en nedbrytningsmetod på Matrix4
- Tillåt användaren att bryta ner transforma matris till översättning/skala/rotation/skew/perspektiv.
- Lagt till en ny Constructor på Vector4 för att få en Vector3 parameter.
- Gör det enklare att konstruera en Vector4 baserat på en vektor3.
- Lagt till en ny överbelastning för Geometri.CreateElement och Geometri.CreateElementUV.
- Tillåter användaren att skapa ett nytt vertex-element och tilldela referensläge/mappläge på en gång, för att göra koden kortare.
- Ändrad LayeredTexture.Textures typ från ICollection till IList
- Tillåt användaren att komma åt lagertexturerna per index.
- Innehållsegenskap i textura
- Tillåt användaren att inbädda rå texturdata inuti texture instansen för FBX filer.
#### **Skapa Vertex genom att tilldela referens- och kartläggningslägen**
Utvecklare kan skapa vertex genom att tilldela referens- och kartläggningslägen i en enda rad av kod. Exempelkod:[Ställ in normala eller UV på kuben](/3d/sv/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/).
#### **Universal 3D Spara alternativet läggs till i filformatet**
Den Universal 3D formatalternativ har lagts till i FileFormat enum.
#### **Inbädda rått innehåll i texturen av FBX**
Den<tt>Innehåll</tt>Egenskapen har lagt till i<tt>Textur</tt>Klass för att lägga in det råa innehållet i texturen i dokumentet FBX. Exempelkod:[Lägg till material till kubenen](/3d/sv/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/#SetupnormalsorUVontheCubeandAddmaterialtothecube-Addmaterialtothecube).
#### **Nedbrytningsmetod läggs till i Matrix4-klassen**
Det är en matematisk verktygsfunktion som används för att bryta ned en affine transformationsmatris.
#### **En ny konstruktör i Vector4 klass läggs till för att få en Vector3-objektparameter parameter.**
Det gör det lättare att konstruera en vektor4 baserat på vektor3. Det fjärde värdet av vektor4 presenterar plan w och dess standardvärde är 1..
