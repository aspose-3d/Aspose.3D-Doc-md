---
title: FAQs
type: docs
weight: 170
url: /sv/python-net/faqs/
description: Vanliga frågor om Aspose.3D för . Netto.
---
####  **Q: Hur animerar man FBX eller annat 3D-formats särskilda egenskaper som inte definierades i Aspose.3D?**
*A**: Skapa en dynamisk egenskap på målobjektet och utför animation av egenskaper på den dynamiska egenskapen, eftersom egenskapen beror på konkret filformat, Aspose. 3D kan inte garantera att animationen kan fungera när du sparar scenen till en annan formattyp.
####  **Q: Varför inte animeringen på scenens rotnod fungerar när den serieliseras till FBX-fil?**
*A**: Formatet FBX låter dig inte komma åt rotnodens egenskaper, så animeringen fungerar inte.
####  **Q: Varför jag ändrade tillgångsinfo på scenen, och försöka importera den genererade FBX filen till 3ds max, var alla dessa uppgifter förlorade?**
*A**: 3Ds MAX eller någon annan programvara kan bara importera FBX-filen, men inte öppna filen FBX. Det betyder att det låter dig importera flera FBX inuti en scen, om tillgångsinfo kan användas på den aktuella scenen, då din ursprungliga scen info kan skrivas över genom att importera, Så det är 3Ds MAXs designpolicy att inte importera scenens tillgångsinfo.
