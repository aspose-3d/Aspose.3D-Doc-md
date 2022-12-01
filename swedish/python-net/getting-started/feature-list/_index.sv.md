---
title: Funktionslista
type: docs
weight: 30
url: /sv/python-net/feature-list/
---
Aspose.3D Egenskaper


## **Plattformar som stöds**

Plattformarna Aspose.3D för Python via .NET kan användas på Windows x64 eller x86 och brett sortiment 07611 33481 distributioner med Python 3.5 eller senare installerade. Det finns ytterligare krav på målplattformen Linux:
- GCC-6 körtidsbibliotek (eller senare)
- Beroende på .NET Core Runtime. Installera .NET Core Runtime själv krävs INTE.
- För Python 3.5-3.7: Pymalloc-byggnaden av Python behövs. Alternativet för byggnad --with-pymalloc Python är aktiverat som standard. Typiskt är pymalloc-bygget Python markerat med m sufix i filnamnet.
- Libpython delade Python bibliotek. Alternativet för byggnad Python---enable är inaktiverat som standard, några Python distributioner innehåller inte det delade biblioteket libpython. För vissa linuxplattformar kan det delade libpython biblioteket installeras med pakethanteraren, till exempel: sudo apt-get install libpython3.7. Den vanliga frågan är att libpython biblioteket är installerat på en annan plats än standardsystemplatsen för delade bibliotek. Problemet kan rättas genom att använda Python bygga alternativ för att ställa in alternativa bibliotekssökvägar vid sammanställning . Python, eller fixeras genom att skapa en symbolisk länk till libpython biblioteksfilen i systemets standardplats för delade bibliotek. Vanligtvis är namnet libpython delade biblioteksfilen libpythonX. Hmm. Så... 1. 0 för Python 3,5-3. 7 eller libpythonX. Y... Så... 1. 0 för Python 3,8 eller senare (t.ex. libpython3.7m. Så... 1. - Libpython3.9. Så... 1. ).
- Libgdiplus 6. 0. 1 eller senare


## **Funktionsmatris**

|**Egenskaper** |` `FBX1|` `Collada1|` `glTF1|` `glTF 2,0|` `U3D1|` `PDF1|` `STL1|` `OBJ1|` `PLY1|` `3DS1|` `ASE1|` `X|` `3MF1|` `RVM1|` `Draco1|
|:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |
|` `Lambert Material|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||
|` `Fongmaterial|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||
|` `Shaderbaserat material.|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|||||||||||||
|` `PBR Material||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||||||
|` `PBR Specifika material||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||||||
|` `Diffus|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|||
|` `Avancerad textur|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||
|` `Polygonmaskor|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||
|` ` Triangelbaserade maskor|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|
|` `Vertexämnen|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|
|` `NURBS geometrier|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|||||||||||||||
|` `Parameteriserade geometrier||||||||||||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||
|` `Lokal omvandling|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||
|` `Instans|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||||
|` `Scenegraf|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||
|` `Anpassad egenskap|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||||||
|` `Skelett|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||||||||
|` `Morf deformerare|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||||||||
|` `Property animation|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||||||||||||
|` `Mesh-kompression|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|||||||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>||<p>![TOD:imageName_Av_Text:](accept.png)</p><p> </p>|

