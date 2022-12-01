---
title: Aspose.3D for Java 19,11 Utgivningsmeddelanden
type: docs
weight: 20
url: /sv/java/aspose-3d-for-java-19-11-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for Java 19.11.

{{% /alert %}} 
## **Förbättringar och förändringar**

|` `**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-575 |` `Lägg .ATT filimportstöd.|` `Ny funktion|
|THREEDNET-578 |` `Lägg .ATT filexportstöd|` `Ny funktion|
|THREEDNET-577 |` `Refaktorn[Fastighetssystem](/3d/sv/java/read-3d-document/#read3ddocument-workingwith3dproperties)Aspose.3D|` `Förbättring|
|THREEDNET-583 |` `Genomfört de som inte stöds[RVM enhetstyp](/3d/sv/java/specify-3d-file-save-options/#specify3dfilesaveoptions-useofrvmsaveoptions) |` `Förbättring|
|THREEDNET-580 |` `[FBX Import](/3d/sv/java/specify-3d-file-load-options/#specify3dfileloadoptions-usefbxloadoptions)Undantag|` `Förbättring|
|THREEDNET-579 |` `Problem med omvandling RVM till GLTF|` `Bug|
|THREEDNET-582 |` `Problem med omvandling RVM|` `Bug|
|THREEDNET-585 |` ` Fast valideringsfel för de genererade glTF filer|` `Bug|
## **API ändringar**
### **Lagt till klass com.pose. Threed.FBXLoadOptions.**
När vissa egenskaper definierade i FBX globala inställningssektioner har liknande ersättning i Aspose.ThreeD. De kommer att konsumeras och konverteras till den inhemska egendomen. Därför kan du inte komma åt dem genom den dynamiska egendomen.

Aspose.3D 19.11, du kan använda KeepBuiltinGlobalSettings i FBXLoadOptions för att stänga av denna funktion, och hålla allting i GlobalSettings ofiltrerat.

**Provkod:**

{{< highlight "java" >}}

 //This will output all properties defined in GlobalSettings in FBX file.

Scene scene = new Scene();

FBXLoadOptions opt = new FBXLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

scene.open("test.FBX", opt);

for (Property property : scene.getRootNode().getAssetInfo().getProperties()) {

     System.out.println(property);

}

{{< /highlight >}}
### **Lagt till klass com.aspose. Threed.RvmFormatt**
### **Definition:**
{{< highlight "java" >}}



/**

 * The RVM Format

 */

public class RvmFormat extends FileFormat

{

    /**

     * Load the attributes from specified file name

     * @param scene The scene where the attributes will be applied to

     * @param fileName The file's name that contains the attributes

     * @param prefix The prefix of the attributes that used to avoid conflict of names, default value is "rvm:"

     */

    public void loadAttributes(Scene scene, String fileName, String prefix)

        throws IOException;

    /**

     * Load the attributes from specified file name

     * @param scene The scene where the attributes will be applied to

     * @param fileName The file's name that contains the attributes

     */

    public void loadAttributes(Scene scene, String fileName)

        throws IOException;

    /**

     * Load the attributes from specified stream

     * @param scene The scene where the attributes will be applied to

     * @param stream The stream that contains the attributes

     * @param prefix The prefix of the attributes that used to avoid conflict of names, default value is "rvm:"

     */

    public void loadAttributes(Scene scene, Stream stream, String prefix)

        throws IOException;

    /**

     * Load the attributes from specified stream

     * @param scene The scene where the attributes will be applied to

     * @param stream The stream that contains the attributes

     */

    public void loadAttributes(Scene scene, Stream stream)

        throws IOException;

}

{{< /highlight >}}

Detta gör det möjligt för användaren att manuellt ladda . Att filen och bifoga metadata till en angiven scen instans, användbar när den . Att filen kan inte hittas av Aspose.3D.

Provkod:

{{% alert color="primary" %}} 

Scene = ny Scene(@"detta mapp\test.rvm");
Filformat.RVM_ BINARY.loadAttributes( scen, @"That mapp\ test.att");

{{% /alert %}} 
### **Lagt till medlemmar i klassen com.aspose.3reed.RvmLoadOptions.**
{{% alert color="primary" %}} 

/**
\* Får prefixet för attribut som definierades i externa attributfiler,
\* Prefixet används för att undvika namnkonflikter, standardvärdet är "rvm:"
*/
Offentlig sträng fåAttributePrefix ();

/**
\* Anger prefixet för attribut som definierades i externa attributfiler,
\* Prefixet används för att undvika namnkonflikter, standardvärdet är "rvm:"
\* @Param värde Nytt värde
*/
Public void setAttributePrefix(String value)

Privat sträng attributPrefix;
/**
\* Hämtar om attribut ska laddas från extern egenskapslistfil(. t /. attrib /. (txt), standardvärde är sant.
*/
Public boolean getLookupAttributes ();

/**
\* Ställer in om attribut ska laddas från extern egenskapslistfil(. t /. attrib /. (txt), standardvärde är sant.
\* @Param värde Nytt värde
*/
Public void setLookupAttributes(boolean value;

{{% /alert %}} 
### **Lagt till medlemmar i klassen com.aspose.3reed.RvmSaveOptions.**
{{< highlight "java" >}}

     /**

     * Gets the prefix of which attributes that will be exported, the exported property will contains no prefix, custom properties with different prefix will not be exported, default value is 'rvm:'.

     * For example if a property is rvm:Refno=345, the exported attribute will be Refno = 345, the prefix is stripped.

     */

    public String getAttributePrefix();



    /**

     * Sets the prefix of which attributes that will be exported, the exported property will contains no prefix, custom properties with different prefix will not be exported, default value is 'rvm:'.

     * For example if a property is rvm:Refno=345, the exported attribute will be Refno = 345, the prefix is stripped.

     * @param value New value

     */

    public void setAttributePrefix(String value);



    private String attributePrefix;

    /**

     * Gets the file name of attribute list file, exporter will generate a name based on the .rvm file name when this property is undefined, default value is null.

     */

    public String getAttributeListFile();



    /**

     * Sets the file name of attribute list file, exporter will generate a name based on the .rvm file name when this property is undefined, default value is null.

     * @param value New value

     */

    public void setAttributeListFile(String value);



    /**

     * Gets whether to export the attribute list to an external .att file, default value is false.

     */

    public boolean getExportAttributes();



    /**

     * Sets whether to export the attribute list to an external .att file, default value is false.

     * @param value New value

     */

    public void setExportAttributes(boolean value);


{{< /highlight >}}



**Urvalskod**

{{< highlight "java" >}}

 Scene scene = new Scene();

        Node node = scene.getRootNode().createChildNode("Box", new Box());

        node.setProperty("rvm:Refno", "=3462123");

        node.setProperty("rvm:Description", "This is the description of the box");

        RvmSaveOptions opt = new RvmSaveOptions();

        //The RVM attribute's prefix is rvm:, all properties that starts with rvm: will be exported to .att file(the prefix will be removed)

        opt.setAttributePrefix("rvm:");

        opt.setExportAttributes(true);

        scene.save("test.rvm", opt);

{{< /highlight >}}
### **Tillagd fastighet Egenskaper till klass com.aspose.threed.A3DObjekt**
{{< highlight "java" >}}

     /**

     * Gets the collection of all properties.

     */

    public PropertyCollection getProperties();

{{< /highlight >}}
### **Tillagd klass com.pose. tre.Property Collections**
{{< highlight "java" >}}

     /**

 * The collection of properties

 */

public class PropertyCollection implements Iterable<Property>

{

    /**

     * Gets the count of declared properties.

     */

    public int size();



    /**

     * Gets the property by index.

     * @param idx 

     */

    public Property get(int idx);



    /**

     * Finds the property.

     * It can be a dynamic property (Created by CreateDynamicProperty/SetProperty)

     * or native property(Identified by its name)

     * @param property Property name.

     * @return The property.

     */

    public Property findProperty(String property);

    /**

     * Gets the value of the property by property name.

     * @param property The name of the property

     */

    public Object get(String property);



      /**

     * Sets the value of the property by property name.

     * @param property The name of the property

     * @param value New value

     */

    public void set(String property, Object value);



    /**

     * Removes a dynamic property.

     * @param property Which property to remove

     * @return true if the property is successfully removed

     */

    public boolean removeProperty(Property property);



    /**

     * Removes a dynamic property.

     * @param property Which property to remove

     * @return true if the property is successfully removed

     */

    public boolean removeProperty(String property);



    /**

     * Returns an enumerator that iterates through the collection.

     */

    @Override

    public Iterator<Property> iterator();



}

{{< /highlight >}}

**Urvalskod**

{{< highlight "java" >}}

Scenen = ny Scene ("Camera.fbx");

Material = scene.getRootNode().getChildNodes().get(0).getMaterial();

Property Collection props = material.getProperties();

//Lista alla egenskaper med hjälp av foreachs

För(Property: rekvisit)

            *

System.out.printf ("%s = %s\n", prop.getName

}

//Eller att använda ordinal för loop

För(int i = 0; i< props.size(); i++)

            {

                Property prop = props.get(i);

                System.out.printf("%s = %s", prop.getName(), prop.getValue());

            }

            //Get property value by name

            Object diffuse = props.get("Diffuse");

            System.out.println(diffuse);

            //modify property value by name

            props.set("Diffuse", new Vector3(1, 0, 1));

            //Get property instance by name

            Property pdiffuse = props.findProperty("Diffuse");

            System.out.println(pdiffuse);

            //Since Property is also inherited from A3DObject

            //It's possible to get the property of the property

            System.out.printf("Property flags = %s\n", pdiffuse.getProperty("flags"));

            //and some properties that only defined in FBX file:

            System.out.printf("Label = %s\n", pdiffuse.getProperty("label"));

            System.out.printf("Type Name = %s\n", pdiffuse.getProperty("typeName"));

            //so traversal on property's property is possible

            for(Property pp : pdiffuse.getProperties())

            {

                System.out.printf("Diffuse.{0} = {1}", pp.getName(), pp.getValue());

            }

{{< /highlight >}}
