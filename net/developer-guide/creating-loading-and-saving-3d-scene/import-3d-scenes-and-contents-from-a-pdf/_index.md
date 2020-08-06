---
title: Import 3D Scenes and Contents from a PDF
type: docs
weight: 50
url: /net/import-3d-scenes-and-contents-from-a-pdf/
---

{{% alert color="primary" %}} 

The [Scene](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Scene) class of the Aspose.3D API represents a 3D scene. Developers can extract 3D scenes and contents from a PDF file.

{{% /alert %}} 
## **Open Scene from a Password Protected PDF**
The Open method of the Scene class allows to load the 3D scene from an input PDF file. Developers may also apply password for the protected PDFs using [PdfLoadOptions](http://www.aspose.com/api/net/3d/aspose.threed.formats/pdfloadoptions) class as shown in this code example:

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
## **Extract All Raw 3D Contents from a PDF**
The Extract method of the [PdfFormat](http://www.aspose.com/api/net/3d/aspose.threed.formats/pdfformat) class allows to extract 3D contents from a PDF file. Developers may iterate through the contents, and save them into the separate files as shown in this code example:

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
## **Extract All 3D Scenes and Save them into Supported 3D Formats**
The ExtractScene method of the [PdfFormat](http://www.aspose.com/api/net/3d/aspose.threed.formats/pdfformat) class allows to extract 3D scenes from a PDF file. Developers may iterate through the scenes, and save them in the supported 3D file formats as shown in this code example:

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}} 

All the supported 3D file formats are listed in the [Product Overview](http://www.aspose.com/docs/display/3dnet/Product+Overview) page.

{{% /alert %}}
