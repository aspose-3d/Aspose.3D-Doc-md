---
title: Ange 3D Ladda alternativ för fil i C#
linktitle: Ange 3D Ladda alternativ för filName
type: docs
weight: 30
url: /sv/net/specify-3d-file-load-options/
description: Det finns flera Scene.Öppen metod överbelastning eller Scene klass konstruktor överbelastning som accepterar ett LoadOptions objekt. Varje lastformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet.
---
##  **Översikt**

Den här artikeln förklarar hur du kan ladda olika typer av 3D genom att använda deras respektive laddningsalternativ klasser i C# Scene-objektet och sedan kan du [Spara den i olika 3D som stöds](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Genom att ladda och spara kan du utföra antal olika konverteringar, t.ex.

- Konvertera FBX till OBJ i C#
- Konvertera 3DS till FBX i C#
- Konvertera U3D till OBJ i C#
- Konvertera OBJ till 3DS i C#
- Konvertera X till 3DS i C#

##  **3D Ladda ner filer**
Det finns flera överbelastningar av [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) metoden eller överbelastningar av konstruktörsklass som accepterar ett `LoadOptions`-objekt. Detta bör vara ett föremål för en klass som härrör från klassen `LoadOptions`. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns `ColladaSaveOptions` för `FileFormat.Collada` spara formatet.
###  **Use of the Discreet 3DS Load Options**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en Diskret 3DS-fil lads.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
###  **Användning av Obj-lastalternativ**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en 3D Obj-fil laddas.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
###  **Användning av laddandealternativ för STLName**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en STL-fil lads.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
###  **Användning av laddandealternativ för U3DName**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en U3D-fil laddas.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
###  **Användning av laddandealternativ för glTFName**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en glTF-fil laddas.
####  **Vänd V/T texturkoordinat**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
###  **Användning av Ply-lastalternativ**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en PLY-modell lads.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
###  **Användning av DirectX X-lastalternativ**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en DirectX-fil laddas.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
###  **Use RVM load options**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
###  **Using FBX Load Options**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
