---
title: 3D sahnelerini ve içeriğini PDF 'dan içe aktarın
type: docs
weight: 50
url: /tr/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.
---
{{% alert color="primary" %}}

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.

{{% /alert %}}
##  **Bir şifre korumalı PDF açık sahne**
`Scene` sınıfının `open` yöntemi, 3D sahnesini bir giriş PDF dosyasından yüklemeye izin verir. Geliştiriciler ayrıca bu kod örneğinde gösterildiği gibi [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) sınıfını kullanarak korunan pdf'ler için şifre de uygulayabilir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
##  **Tüm ham 3D içeriğini PDF 'dan ayıklayın**
The `extract` method of the [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) class allows to extract 3D contents from a PDF file. Developers may iterate through the contents, and save them into the separate files as shown in this code example:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
##  **Extract All 3D Scenes and Save them into Supported 3D Formats**
`PdfFormat` sınıfının `extract_scene` yöntemi, PDF dosyasından 3D sahnelerini çıkarmanıza izin verir. Geliştiriciler sahneler aracılığıyla yineleyebilir ve bu kod örneğinde gösterildiği gibi desteklenen 3D dosya formatlarında kaydedebilir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Desteklenen tüm 3D dosya biçimleri [Product Overview](/3d/tr/python-net/product-overview/) sayfasında listelenir.

{{% /alert %}}
