---
title: Aspose.3D for .NET 19,11 Utgivningsmeddelanden
type: docs
weight: 20
url: /sv/net/aspose-3d-for-net-19-11-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for .NET 19.11.

{{% /alert %}} 
## **Förbättringar och förändringar**

|` `**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-575 |` `Lägg .ATT filimportstöd.|` `Ny funktion|
|THREEDNET-578 |` `Lägg .ATT filexportstöd|` `Ny funktion|
|THREEDNET-577 |` `Refaktorn[Fastighetssystem](/3d/sv/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-workingwith3dsceneproperties)Aspose.3D|` `Förbättring|
|THREEDNET-583 |` `Genomfört de som inte stöds[RVM enhetstyp](/3d/sv/net/specify-3d-file-save-options/#specify3dfilesaveoptions-useofthervmsaveoptions) |` `Förbättring|
|THREEDNET-580 |` `[FBX Import](/3d/sv/net/specify-3d-file-load-options/#specify3dfileloadoptions-usingfbxloadoptions)Undantag|` `Förbättring|
|THREEDNET-579 |` `Problem med omvandling RVM till GLTF|` `Bug|
|THREEDNET-582 |` `Problem med omvandling RVM|` `Bug|
|THREEDNET-585 |` ` Fast valideringsfel för de genererade glTF filer|` `Bug|
## **API ändringar**
### **Lagt till klass Aspose.ThreeD. Format.FBXLoadOptionsName**
När vissa egenskaper definierade i FBX globala inställningssektioner har liknande ersättning i Aspose.ThreeD. De kommer att konsumeras och konverteras till den inhemska egendomen. Därför kan du inte komma åt dem genom den dynamiska egendomen.

Aspose.3D 19.11, du kan använda KeepBuiltinGlobalSettings i FBXLoadOptions för att stänga av denna funktion, och hålla allting i GlobalSettings ofiltrerat.

**Provkod:**

{{< highlight "java" >}}

 //This will output all properties defined in GlobalSettings in FBX file.

Scene scene = new Scene();

var opt = new FBXLoadOptions() { KeepBuiltinGlobalSettings = true };

scene.Open(@"test.FBX", opt);

foreach (Property property in scene.RootNode.AssetInfo.Properties)

{

     Console.WriteLine(property);

}

{{< /highlight >}}
### **Lagt till klass Aspose.ThreeD.Formats.RvmFormatt**
Definition:

{{< highlight "java" >}}

     /// <summary>

    /// The RVM Format

    /// </summary>

    public class RvmFormat : FileFormat

    {

        /// <summary>

        /// Load the attributes from specified stream

        /// </summary>

        /// <param name="scene">The scene where the attributes will be applied to</param>

        /// <param name="stream">The stream that contains the attributes</param>

        /// <param name="prefix">The prefix of the attributes that used to avoid conflict of names, default value is "rvm:"</param>

        public void LoadAttributes(Scene scene, Stream stream, string prefix = "rvm:");

        /// <summary>

        /// Load the attributes from specified file name

        /// </summary>

        /// <param name="scene">The scene where the attributes will be applied to</param>

        /// <param name="fileName">The file's name that contains the attributes</param>

        /// <param name="prefix">The prefix of the attributes that used to avoid conflict of names, default value is "rvm:"</param>

        public void LoadAttributes(Scene scene, string fileName, string prefix = "rvm:");

    }


{{< /highlight >}}

Detta gör det möjligt för användaren att manuellt ladda . Att filen och bifoga metadata till en angiven scen instans, användbar när den . Att filen kan inte hittas av Aspose.3D.

Provkod:

{{% alert color="primary" %}} 

Scene = ny Scene(@"detta mapp\test.rvm");
Arkivform.RvmBinary.LoadAttributes(scene, @"That folder\test.att");

{{% /alert %}} 
### **Lagt till medlemmar i klass Aspose.ThreeD.Formats.RvmLoadOptions.**


{{% alert color="primary" %}} 

/// <summary>
/// Får eller ställer in prefixet för attribut som definierades i externa attributfiler,
/// Prefixet används för att undvika namnkonflikter, standardvärdet är "rvm:"
/// </summary>
Public String AttributPrefix { get; set; }

/// <summary>
/// Hämtar eller ställer in om attribut ska laddas från extern egenskapslistfil(. t /. attrib /. (txt), standardvärde är sant.
/// </summary>
Public bools UppsökningAttributes { get; set; }

{{% /alert %}} 
### **Lagt till medlemmar i klass Aspose.ThreeD.Formats.RvmSaveOptions.**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the prefix of which attributes that will be exported, the exported property will contains no prefix, custom properties with different prefix will not be exported, default value is 'rvm:'.

/// For example if a property is rvm:Refno=345, the exported attribute will be Refno = 345, the prefix is stripped.

/// </summary>

public string AttributePrefix { get; set; }

/// <summary>

/// Gets or sets the file name of attribute list file, exporter will generate a name based on the .rvm file name when this property is undefined, default value is null.

/// </summary>

public string AttributeListFile { get; set; }

/// <summary>

/// Gets or sets whether to export the attribute list to an external .att file, default value is false.

/// </summary>

public bool ExportAttributes { get; set; }


{{< /highlight >}}



**Urvalskod**

{{< highlight "java" >}}

 Scene scene = new Scene();

var node = scene.RootNode.CreateChildNode("Box", new Box());

node.SetProperty("rvm:Refno", "=3462123");

node.SetProperty("rvm:Description", "This is the description of the box");

//The RVM attribute's prefix is rvm:, all properties that starts with rvm: will be exported to .att file(the prefix will be removed)

var opt = new RvmSaveOptions() { AttributePrefix = "rvm:", ExportAttributes = true };

scene.Save("test.rvm", opt);

{{< /highlight >}}
### **Tillagd fastighet Egenskaper till klass Aspose.ThreeD.A3DObject**


{{< highlight "java" >}}

 /// <summary>

/// The properties of the current object.

/// </summary>

Aspose.ThreeD.PropertyCollection Properties{ get;}

{{< /highlight >}}


### **Tillagd klass Aspose.ThreeD.Property Collections**
{{< highlight "java" >}}

     /// <summary>

    /// The collection of properties

    /// </summary>

    public class PropertyCollection : IEnumerable<Property>

    {

        /// <summary>

        /// Gets the count of declared properties.

        /// </summary>

        public int Count { get; }

        /// <summary>

        /// Gets the property by index.

        /// </summary>

        /// <param name="idx">The 0-based index of the property</param>

        /// <returns></returns>

        public Property this[int idx] { get; }

        /// <summary>

        /// Finds the property.

        /// It can be a dynamic property (Created by CreateDynamicProperty/SetProperty) 

        /// or native property(Identified by its name)

        /// </summary>

        /// <returns>The property.</returns>

        /// <param name="property">Property name.</param>

        public Property FindProperty(string property);

        /// <summary>

        /// Gets or sets the value of the property by property name.

        /// </summary>

        /// <param name="property">The name of the property</param>

        /// <returns>The property's value</returns>

        public object this[string property] {get; set; }

        /// <summary>

        /// Removes a dynamic property.

        /// </summary>

        /// <param name="property">Which property to remove</param>

        /// <returns>true if the property is successfully removed</returns>

        public bool RemoveProperty(Property property);

        /// <summary>

        /// Removes a dynamic property.

        /// </summary>

        /// <param name="property">Which property to remove</param>

        /// <returns>true if the property is successfully removed</returns>

        public bool RemoveProperty(string property);

        /// <summary>

        ///  Returns an enumerator that iterates through the collection.

        /// </summary>

        /// <returns></returns>

        public IEnumerator<Property> GetEnumerator();

    }

{{< /highlight >}}

**Urvalskod**

{{< highlight "java" >}}

Scenen = ny Scene(@"Camera.fbx");

Material = scen.RootNode.ChildNodes[0].Material;

Property Collection props = material. Egenskaper;

//Lista alla egenskaper med hjälp av foreachs

Föreach (var prop i rekvisita)

            *

Console.WriteLine ("{0} = {1}", prop.namn, prop.värde);

}

//Eller att använda ordinal för loop

För(int i = 0; i< props.Count; i++)

            {

                var prop = props[i];

                Console.WriteLine("{0} = {1}", prop.Name, prop.Value);

            }

            //Get property value by name

            var diffuse = props["Diffuse"];

            Console.WriteLine(diffuse);

            //modify property value by name

            props["Diffuse"] = new Vector3(1, 0, 1);

            //Get property instance by name

            Property pdiffuse = props.FindProperty("Diffuse");

            Console.WriteLine(pdiffuse);

            //Since Property is also inherited from A3DObject

            //It's possible to get the property of the property

            Console.WriteLine("Property flags = {0}", pdiffuse.GetProperty("flags"));

            //and some properties that only defined in FBX file:

            Console.WriteLine("Label = {0}", pdiffuse.GetProperty("label"));

            Console.WriteLine("Type Name = {0}", pdiffuse.GetProperty("typeName"));

            //so traversal on property's property is possible

            foreach(var pp in pdiffuse.Properties)

            {

                Console.WriteLine("Diffuse.{0} = {1}", pp.Name, pp.Value);

            }

{{< /highlight >}}
