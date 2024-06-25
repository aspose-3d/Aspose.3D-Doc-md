---
title: Använd visuella effekter vid sparning av 3D Visningar
type: docs
weight: 10
url: /sv/python-net/apply-visual-effects-on-saving-3d-views/
description: Med Aspose.3D for Python via .NET API kan utvecklare använda visuella effekter på 3D vyer innan de sparar i bilden. Dessa visuella effekter kallas också de efterbehandlingseffekter eller filter som används i realtid för allt som visas i 3D Visa.
---
{{% alert color="primary" %}}

Med [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/) kan utvecklare använda visuella effekter på 3D vyer innan bilden sparas. Dessa visuella effekter kallas också de efterbehandlingseffekter eller filter som används i realtid för allt som visas i 3D Visa.

{{% /alert %}}
##  **Använd visuella effekter på 3D Visa**
[`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing)-metoden för [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer)-klassen gör det möjligt att skapa en visuell effekt som stöds. `Renderer`-klassen erbjuder en [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings)-medlem att applicera olika filter, metoden Lägg till för klassen `PostProcessings` låter inkorporera ett filter innan rendering.
###  **Programmeringsprova**
Det här kodexemplet gäller visuell effekt på en 3D-vy.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
