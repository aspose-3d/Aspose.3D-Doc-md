---
title: 3D dosyasının biçimini algılama
type: docs
weight: 10
url: /tr/java/detect-format-of-3d-file/
description: Aspose.3D for Java API, dosya uzantısının dosya içeriğinin uygun olduğunu garanti etmediği için açmadan önce 3D desteklenen biçimleri tespit etme desteğine sahiptir.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API, dosya uzantısının dosya içeriğinin uygun olduğunu garanti etmediği için açmadan önce 3D desteklenen biçimleri tespit etme desteğine sahiptir.

{{% /alert %}} 
##  **Detect Format rorogramming ample ample**
Kaynak kodu, dosya formatını (dosya yolunu veya akışını kullanarak) nasıl tespit edeceğinizi ve uzantısını kontrol edeceğinizi gösterir.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// detect format of 3D file
FileFormat inputFormat = FileFormat.detect(MyDir + "document.fbx");
// display the file format
System.out.println("File Format: " + inputFormat.toString());
{{< /highlight >}}




