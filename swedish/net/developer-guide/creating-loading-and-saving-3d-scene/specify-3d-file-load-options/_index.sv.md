---
title: Ange 3D Filladdningsalternativ i C#
linktitle: Ange 3D Filladdningsalternativ
type: docs
weight: 30
url: /sv/net/specify-3d-file-load-options/
description: Det finns flera Scene.Öppen metod överbelastning eller Scene klass konstruktor överbelastning som accepterar ett LoadOptions objekt. Varje lastformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet.
---
## **Översikt**

Den här artikeln förklarar hur du kan ladda olika typer av 3D filer med deras respektive belastningsalternativ klasser i 07. 6113481 inuti Scene-objektet och sedan kan du[Spara den i olika 3D stödda filformat](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Genom att ladda och spara kan du utföra antal olika konverteringar, t.ex.

- Konvertera FBX till OBJ i C#
- Konvertera 3DS till FBX i C#
- Konvertera U3D till OBJ i C#
- Konvertera OBJ till 3DS i C#
- Konvertera X till 3DS i C#

## **3D Filladdningsalternativ**
Det finns flera metodöverbelastningar [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) eller Scene klass konstruktor överbelastningar som accepterar ett `LoadOptions` objekt. Detta bör vara föremål för en klass som härrör från klassen `LoadOptions`. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns det `ColladaSaveOptions` för `FileFormat.Collada` sparformat.
### **Användning av diskret 3DS lastalternativ**
Koden C# nedan visar hur man ställer in belastningsalternativ innan man laddar en diskret 3DS-fil.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **Användning av Obj-lastalternativ**
Koden C# nedan visar hur man ställer in belastningsalternativ innan man laddar en 3D Obj-fil.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **Användning av belastningsalternativ STL**
Koden C# nedan visar hur man ställer in belastningsalternativ innan man laddar en STL-fil.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **Användning av belastningsalternativ U3D**
Koden C# nedan visar hur man ställer in belastningsalternativ innan man laddar en U3D-fil.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **Användning av belastningsalternativ glTF**
Koden C# nedan visar hur man ställer in belastningsalternativ innan man laddar en glTF-fil.
#### **Vänd V/T texturkoordinat**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **Användning av Ply-lastalternativ**
Koden C# nedan visar hur man ställer in belastningsalternativ innan man laddar en PLY modell.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **Användning av DirectX X-lastalternativ**
Koden C# nedan visar hur man ställer in belastningsalternativ innan man laddar en DirectX X-fil.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **Använd RVM belastningsalternativ**
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
### **Använda FBX lastalternativ**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
