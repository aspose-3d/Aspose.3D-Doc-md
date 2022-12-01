---
title: Aspose.3D for .NET 1.2.0 Utgivning
type: docs
weight: 10
url: /sv/net/aspose-3d-for-net-1-2-0-release-notes/
---
Följande är en förteckning över förbättringar och förändringar i denna publicering av Aspose.3D
# **1)Aspose.3D**
## **Nya funktioner**
(THREEDNET-115) - 3DS(Filformat för Autodesk 3D Studio DOS) importör och exportör
## **Förbättringa**
(THREEDNET-122) - Stöd för flera scener

(THREEDNET-123) - Tillåt användaren att vända koordinatsystem i OBJ/3DS/STL
# **Offentlig API och bakåts oförenliga förändringar**
Nedan följer en förteckning över eventuella ändringar i allmänheten API, t.ex. Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon ändring som listas, vänligen ta upp det på supportforumet Aspose.3D.

Tillagd egenskap Mål / Direktion på Ljus/kamera

Collada/3ds och några andra filer använder Target/Direction för att ange ljus/kameras orientering.

Lagt till fler medlemsmetoder och operatör överbelastningar för Vector2/Quaternion.

Den används för intern beräkning, och även användbar för kunder.

Lagt till en ny klass PolygonModifier.

Vissa filformat stöder endast triangelnät medan Aspose.3D stöder polygon maskor, så vi lade till denna klass för att tillåta konvertera en polygon-baserade maskor till triangel-baserade maskor.
Vi lägger till fler mesh modifieringar i framtiden.

Lagt till flera IOConfig underklasser som FBXConfig/OBJConfig/STLConfig/Discreet3 DDSConfig

Tillåt användaren att ställa in alternativ under import/exportering som 3ds max/Maya/blender gjorde.
