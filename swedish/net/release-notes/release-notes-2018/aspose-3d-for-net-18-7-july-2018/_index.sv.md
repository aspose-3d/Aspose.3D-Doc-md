---
title: Aspose.3D for .NET 18,7 – juli 2018
type: docs
weight: 60
url: /sv/net/aspose-3d-for-net-18-7-july-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 18,7](https://www.nuget.org/packages/Aspose.3D/18.7.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-405|Lägg till Draco 2.2 importstöd|Ny funktion|
|THREEDNET-406|Lägg till Draco 2.2 exportstöd|Ny funktion|
|THREEDNET-408|Importera glTF filer med dracokomprimering|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **API ändringar**
Två stora förändringar sker:

1. Ta bort några föråldrade klasser och metoder enligt schema, alla XXXXConfig klasser tas bort, användaren bör använda XXXXSaveOptions och XXXXLoadOptions som introducerades 2016.
1. Fil import/export, dessa ändringar gör inga ändringar i gränssnittet.
1. Google Draco import-/exportstöd har uppdaterats till den senaste versionen.
1. Aspose.3D 18.7 Kan importera glTF 2.0 som aktiverat draco komprimering.
#### **Avlägsnad klass Aspose.ThreeD.Formats.Discreet3DSConfig**
#### **Avlägsnad klass Aspose.ThreeD.Formats.FBXConfig**
#### **Avlägsnad klass Aspose.ThreeD. Format.ObjConfig**
#### **Avlägsnad klass Aspose.ThreeD.Formats.STLConfig**
#### **Avlägsnad klass Aspose.ThreeD.Formats.Universal3DConfig**
#### **3 borttagna medlemmar från klass Aspose.ThreeD.A3DObjekt**
{{< highlight "java" >}}

         public Aspose.ThreeD.Property CreateDynamicProperty(string propName, System.Type type)

        public Aspose.ThreeD.Property CreateDynamicProperty(string propName)

        public Aspose.ThreeD.Property GetDynamicProperty(string propName)

{{< /highlight >}}

Använd GetProperty/SetProperty istället, GetProperty/SetProperty läggs till i 17.12.
#### **3 avlägsnade medlemmar från klass Aspose.ThreeD.Animation.Curve:**
{{< highlight "java" >}}

         public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time)

        public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time, float value)

        public Aspose.ThreeD.Animation.KeyFrame CreateKeyFrame(double time, float value, Aspose.ThreeD.Animation.Interpolation interpolation)

{{< /highlight >}}

Använd Lägg till istället, Lägg till i 17.9, Användning Lägg till istället för annat namn kan använda sig av C#: s kollektions initializer syntax(<https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/object-and-collection-initializers>)
#### **3 medlemmar avlägsnade från klass Aspose.ThreeD.Ev:**
{{< highlight "java" >}}

         public bool HasFlags(Aspose.ThreeD.PropertyFlags f)

        string ExtraData{ get;set;}

        Aspose.ThreeD.PropertyFlags Flags{ get;}

{{< /highlight >}}

Dessa är markerade som föråldrade sedan 18,2 de är huvudsakligen för intern användning.
#### **4 metoder avlägsnas från klass Aspose.ThreeD.Scene:**
{{< highlight "java" >}}

         public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.IOConfig config)

        public void Open(string fileName, Aspose.ThreeD.Formats.IOConfig config)

        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.IOConfig config)

        public void Save(string fileName, Aspose.ThreeD.Formats.IOConfig config)

{{< /highlight >}}

Eftersom vi har XXXXSaveOptions/XXXXLoadOptions att ersätta XXXXConfig, dessa metoder blir värdelösa efter avlägsnande XXXXConfig.
#### **3 metoder avlägsnas från klass Aspose.ThreeD.Användningar.Quaternion:**
{{< highlight "java" >}}

         public double GetPitch()

        public double GetYaw()

        public double GetRoll()

{{< /highlight >}}

Dessa är markerade som föråldrade i 18.2, det finns ersättningsmetod EulerAngles ().
#### **1 objekt lagt till i klass Aspose.ThreeD.Formats.ObjLoadOptions:**
{{< highlight "java" >}}

         bool NormalizeNormal{ get;set;}

{{< /highlight >}}

Får eller ställer in om den normala vektorn ska normaliseras under laddningen. Standardvärdet är sant.
##### **Provkod:**
{{< highlight "java" >}}

         Scene scene = new Scene();

        scene.Open("test.obj", new ObjLoadOptions() {NormalizeNormal = false});

{{< /highlight >}}

Detta kommer att ladda obj- filen och lämna de normala vektorerna onormala, Den gamla versionen normaliserar de vanliga vektorerna när obj-filen laddas.
