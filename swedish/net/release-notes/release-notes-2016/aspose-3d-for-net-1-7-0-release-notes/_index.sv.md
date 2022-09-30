---
title: Aspose.3D for .NET 1,7.0 Utgivning
type: docs
weight: 60
url: /sv/net/aspose-3d-for-net-1-7-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 1,7,0](https://www.nuget.org/packages/Aspose.3D/1.7.0)

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-141|Lägg till stöd för att konvertera STL till ett bildformat.|Ny funktion|
|THREEDNET-169|Gör scenen till en textur.|Ny funktion|
|THREEDNET-170|Lägg till stöd för skugga.|Ny funktion|
|THREEDNET-174|Generera normala data från utjämningsgrupp.|Ny funktion|
|THREEDNET-179|Index utanför intervallet uppstod fel vid laddning av en fil U3D.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se listan för eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till Aspose.ThreeD.Enheter.Frustum klass**
En ny klass Frustum läggs till. Kamera och Ljus var underklasserna i enhetsklass. I version 1.7. Dessa klasser är ärvda från Frustum och Frustum ärvs från Entity, eftersom egenskaperna Position, Up, LookAt, Riktning, Target, NearPlane och FarPlane extraheras till Frustum.
#### **Lägger till Aspose.ThreeD.ImageRenderOptions klass**
Det tillåter utvecklare att ställa in olika renderingsalternativ som bakgrundsfärg, tillgångskatalogen och aktivera/insaktivera objektskugga innan en 3D fil konverteras till bild.
#### **Lägger till flera Render metoder i Aspose.ThreeD.Scene klass**
Det återger en 3D scen i givna kamerans perspektiv i angiven bildfilformat och storlek.
#### **Lägger till MoveForward metod i Aspose.ThreeD.Enheter.Kamerklass**
Den går framåt kameran mot sin orientering. Kamerans orientering anges av något av Target/Direction/LookAt

- **Mål:**En målnod i rymden kommer kameran alltid att titta på detta mål oavsett mål/kameran har ändrat sin position i rymden.
- **Utsikt:**En fast position i rymden kommer kameran alltid att titta på denna position.
- **Riktning:**En riktningsvektor, en kamerans orientering anges direkt av denna vektor oavsett position.
#### **Lägger till CastShadows and ReceiveShadows medlemmar i Aspose.ThreeD.Enheter.Geometry klass**
Vissa filformat kan lagra skuggrelaterade inställningar i geometri som FBX, och de används också i rendering.
#### **Lägger till GenereraNormal metod i Aspose.ThreeD.Enheter.PolygonModifier klass**
Det gör det möjligt för utvecklare att generera normala data från Mesh instans, om VertexElementSmoothingGroup element definierades på mesh, den genererade normala data kommer att jämnas ut av VertexElementSmoothingGroup.
#### **Lägger till Kontratmetod i Aspose.ThreeD.Utiliteter.Quaternion klass**
Det tillåter utvecklare att sammanföra två rotationsomvandling till en representerad i Quaternion.
