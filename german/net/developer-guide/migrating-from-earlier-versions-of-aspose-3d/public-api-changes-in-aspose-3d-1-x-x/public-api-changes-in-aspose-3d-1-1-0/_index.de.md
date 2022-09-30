---
title: Öffentliche API Änderungen in Aspose.3D 1.1.0
type: docs
weight: 60
url: /de/net/public-api-changes-in-aspose-3d-1-1-0/
---
**Inhalts übersicht**

- [FBX7200ASCII-Saving-Option wird im File Format hinzugefügt](#PublicAPIChangesinAspose.3D1.1.0-FBX7200ASCIISavingOptionisaddedintheFileFormat)
- [FBX7200Binary Saving Option wird im File Format hinzugefügt](#PublicAPIChangesinAspose.3D1.1.0-FBX7200BinarySavingOptionisaddedintheFileFormat)
- [FBX7300ASCII-Saving-Option wird im File Format hinzugefügt](#PublicAPIChangesinAspose.3D1.1.0-FBX7300ASCIISavingOptionisaddedintheFileFormat)
- [Die Option FBX7300Binary Saving wird im File Format hinzugefügt](#PublicAPIChangesinAspose.3D1.1.0-FBX7300BinarySavingOptionisaddedintheFileFormat)
- [Die Option WavefrontOBJ Speichern wird im File Format und FileFormat Type hinzugefügt](#PublicAPIChangesinAspose.3D1.1.0-WavefrontOBJSavingOptionisaddedintheFileFormatandFileFormatType)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 1.0.0 bis 1.1.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **FBX7200ASCII-Saving-Option wird im File Format hinzugefügt**
Die Option FBX7200ASCII-Format wurde in der FileFormat-Enumer hinzugefügt. Es repräsentiert das Dateiformat ASCII FBX mit der Version 7.2.0. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200ASCII);

{{< /highlight >}}

### **FBX7200Binary Saving Option wird im File Format hinzugefügt**
Die Option FBX7200Binary-Format wurde in der FileFormat-Enumer hinzugefügt. Es repräsentiert das binäre Dateiformat FBX mit der Version 7.2.0. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7200Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7200Binary);

{{< /highlight >}}

### **FBX7300ASCII-Saving-Option wird im File Format hinzugefügt**
Die Option FBX7300ASCII-Format wurde in der FileFormat-Enumer hinzugefügt. Es repräsentiert das Dateiformat ASCII FBX mit 7.3.0 Version. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300ASCII format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300ASCII);

{{< /highlight >}}

### **Die Option FBX7300Binary Saving wird im File Format hinzugefügt**
Die Option FBX7300Binary-Format wurde in der FileFormat-Enumer hinzugefügt. Es repräsentiert das binäre Dateiformat FBX mit 7.3.0 Version. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the FBX7300Binary format

scene.Save("C:\\temp\\Output.fbx", FileFormat.FBX7300Binary);

{{< /highlight >}}

### **Die Option WavefrontOBJ Speichern wird im File Format und FileFormat Type hinzugefügt**
Die Format option WavefrontOBJ wurde in den Emen File Format und FileFormat Type hinzugefügt. Es repräsentiert das Obj-Dateiformat von Wavefront. Beispiel code:

**C#**

{{< highlight "csharp" >}}

 // save scene in the WavefrontOBJ format

scene.Save("C:\\temp\\Output.fbx", FileFormat.WavefrontOBJ);

{{< /highlight >}}

