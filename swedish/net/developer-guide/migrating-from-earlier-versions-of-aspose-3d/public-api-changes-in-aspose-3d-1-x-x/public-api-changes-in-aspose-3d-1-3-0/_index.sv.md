---
title: Offentlig API Ändrar i Aspose.3D 1.3.00
type: docs
weight: 40
url: /sv/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Innehåll**

- [Namespace and class name changes](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Create Vertex by Assigning the Reference and Mapping Modes](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [Universal 3D Saving Option is added in the FileFormat](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Embed Raw Content to the Texture of FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Decompose method is added in the Matrix4 class](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [A new constructor in Vector4 class is added to receive a Vector3 object parameter](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar i Aspose. 3D API från version 1.2.0 till 1.3.0, som kan vara av intresse för modul-/programutvecklare. Det omfattar inte bara nya och uppdaterade offentliga metoder. men också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose. 3D.

{{% /alert %}} 
###  **Ändringar av namnrymd och klassnamn**
- Namnrymd Aspose ThreeD.Animationer ändrade till Aspose.ThreeD.Animation
- Klass Aspose.ThreeD.Animations.Animation ändrad till Aspose.ThreeD.Animation.AnimationNode.
- Namnrymd Aspose.ThreeD.IO ändrad till Aspose.ThreeD.Formats
- Namnrymd Aspose ThreeD.Utils ändrad till Aspose.ThreeD.Utilities.
###  **Skapa Vertex genom att tilldela referens- och kartläggningslägen**
Utvecklare kan skapa vertex genom att tilldela referens- och kartläggningslägen i en enda rad av kod. Exempelkod:

{{% alert color="primary" %}} 

Mesh-klassobjektet används i koden. Vi kan [Skapa ett Mesh-klassobjekt som berättat där.](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **Universal 3D Spararalternativ läggs till i filformatet**
Alternativet Universal 3D-format har lagts till i enument FileFormat. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **Bädda in obehandlat innehåll i texturen av FBX @ info: whatsthis**
Den<tt>Innehåll</tt>Egenskapen har lagt till i<tt>Textur</tt>Klass för att lägga in det obehandlade innehållet i texturen för FBX. Exempelkod:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **Nedbrytningsmetod läggs till i Matrix4-klassen**
Det är en matematisk verktygsfunktion som används för att bryta ned en affine transformationsmatris.
###  **En ny konstruktör i Vector4 klass läggs till för att få en Vector3-objektparameter parameter.**
Det gör det lättare att konstruera en vektor4 baserat på vektor3. Det fjärde värdet av vektor4 presenterar plan w och dess standardvärde är 1..
