---
title: Aspose.3D for .NET 20,2 Utgivning
type: docs
weight: 60
url: /sv/net/aspose-3d-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller publiceringsnoter information för Aspose.3D for .NET 20.2

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-612 |` `IFC kompatibel förfarande I form generering|` `Ny funktion|
|THREEDNET-615 |` `IFC kompatibel förfarande C form generering|` `Ny funktion|
|THREEDNET-616 |` `IFC kompatibel förfarande Z form generering|` `Ny funktion|
|THREEDNET-617 |` `IFC kompatibel processuell L form generering|` `Ny funktion|
|THREEDNET-618 |` `IFC kompatibel processuell T-form generering|` `Ny funktion|
|THREEDNET-619 |` `IFC kompatibel processuell U form generering|` `Ny funktion|
|THREEDNET-620 |` `IFC kompatibel processuell rektangel generering|` `Ny funktion|
|THREEDNET-625 |` `IFC kompatibel processuell cirkel generering|` `Ny funktion|
|THREEDNET-626 |` `IFC kompatibel processuell ellips form generering|` `Ny funktion|
|THREEDNET-558 |` `Lägg till stöd för transparens rendering i webben återgivning|` `Förbättring|
|THREEDNET-606 |` `Visa avgränsande ruta om nod valt i webbläsare för tillgångar.|` `Förbättring|
|THREEDNET-613 |` `Lägg till renderingsstöd för forme|` `Förbättring|
|THREEDNET-630 |` `Process hänger vid laddning RVM filer|` `Bug|
|THREEDNET-632 |` ` Undantag vid lastning FBX|` `Bug|
|THREEDNET-629 |` `Undantag vid omvandling GLB till 3d|` `Bug|
|THREEDNET-623 |` `Intels GPU stöds inte av redigeraren Aspose.3D|` `Bug|
|THREEDNET-628 |` ` Undantag vid lastning FBX|` `Bug|
## **Offentlig API och bakåtkompatibla förändringar**
### **Lagt till ny klass Aspose.ThreeD.Profiler.Profil**
Denna klass är basklassen för alla profiler, som kan användas för att skapa parameteriserade maskor. En profilklass representerar en 2D-profil i x-y-plan.

{{< highlight "java" >}}

     /// <summary>

    /// 2D Profile in xy plane

    /// </summary>

    public abstract class Profile : Entity

    {

        /// <summary>

        /// Gets the extent in x and y dimension.

        /// </summary>

        /// <returns></returns>

        public abstract Vector2 GetExtent();

    }

    /// <summary>

    /// The base class of all parameterized profiles.

    /// </summary>

    public abstract class ParameterizedProfile : Profile

    {

    }

{{< /highlight >}}

Alla underklasser av Profil kan omvandlas till 3D mesh genom LinearExtrusion enligt följande provkod:



{{< highlight "java" >}}

 var mesh = new LinearExtrusion(new LShape()

    {

     FilletRadius = 1,

     Width = 4,

     Depth = 7

      }, 1);

Scene s = new Scene(mesh);

s.Save(@"LShape.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
### **Lagt till ny klass Aspose.ThreeD.Profiler.CircleShape**
Egenskaper av CircleShape kan illustreras i figuren nedan.

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_1.png)
### **Lagt till ny klass Aspose.ThreeD.Profiler.CShape**
Egenskaper av CShape kan illustreras i figuren nedan:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_2.png)
### **Lagt till ny klass Aspose.ThreeD.Profiler.EllipseShape**
Egenskaper av EllipseShape kan illustreras i denna figur:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_3.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.HShape**
Egenskaper av HShape kan illustreras i denna figur:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_4.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.LShape**
Egenskaper av LShape kan illustreras i denna figur:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_5.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.RectangleShape**
Egenskaper av rektangelShape kan illustreras i denna figur:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_6.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.TrapeziumShape**
Egenskaper av TrapeziumShape kan illustreras i denna figur:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_7.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.TShape**
TShapes egenskaper kan illustreras i bilden nedan:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_8.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.UShape**
UShapes egenskaper kan illustreras i följande figur:

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_9.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.ZShape**
Egenskaper av ZShape kan illustreras i följande figur.

![TOD:imageName_Av_Text:](aspose-3d-for-net-20-2-release-notes_10.png)


### **Lagt till ny klass Aspose.ThreeD.Profiler.MirroredShape**
Denna profil definierar en ny profil genom att spegla basprofilen om y-axeln.

{{< highlight "java" >}}

 var mesh = new LinearExtrusion(new MirroredProfile(new LShape()

            {

                FilletRadius = 1,

                Width = 4,

                Depth = 7

            }), 1);

Scene s = new Scene(mesh);

s.Save(@"MirroredLShape.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

