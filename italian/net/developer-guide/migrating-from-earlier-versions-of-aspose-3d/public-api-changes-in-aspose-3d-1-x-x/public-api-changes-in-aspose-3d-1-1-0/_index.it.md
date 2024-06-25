---
title: Variazioni pubbliche di API in Aspose.3D 1.1.0
type: docs
weight: 60
url: /it/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Contenuto sommario**

- [FBX7200ASCII Saving Option viene aggiunto nel FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [FBX7200Binary Saving Option viene aggiunto nel FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [L'opzione di risparmio FBX7300ASCII viene aggiunta nel FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [L'opzione di risparmio binario FBX7300viene aggiunta nel FileFormat](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [L'opzione di salvataggio di WavefrontOBJ viene aggiunta in FileFormat e FileFormatType](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche a Aspose.3D API dalla versione da 1.0.0 a 1.1.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.3D.

{{% /alert %}} 
###  **FBX7200ASCII Saving Option viene aggiunto nel FileFormat**
L'opzione di formato FBX7200ASCII è stata aggiunta nell'enum FileFormat. Rappresenta il formato di file ASCII FBX, con la versione 7.2.0. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

###  **FBX7200Binary Saving Option viene aggiunto nel FileFormat**
L'opzione del formato FBX7200Binary è stata aggiunta nell'enum FileFormat. Rappresenta il formato di file Binary FBX, con la versione 7.2.0. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

###  **L'opzione di risparmio FBX7300ASCII viene aggiunta nel FileFormat**
L'opzione di formato FBX7300ASCII è stata aggiunta nell'enum FileFormat. Rappresenta il formato di file ASCII FBX, con la versione 7.3.0. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

###  **L'opzione di risparmio binario FBX7300viene aggiunta nel FileFormat**
L'opzione del formato FBX7300Binary è stata aggiunta nell'enum FileFormat. Rappresenta il formato di file Binary FBX, con la versione 7.3.0. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

###  **L'opzione di salvataggio di WavefrontOBJ viene aggiunta in FileFormat e FileFormatType**
L'opzione di formato WavefrontOBJ è stata aggiunta nelle enums FileFormat e FileFormatType. Rappresenta il formato di file Obj di Wavefront. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

