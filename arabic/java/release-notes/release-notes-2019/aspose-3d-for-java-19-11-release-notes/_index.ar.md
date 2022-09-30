---
title: Aspose.3D for Java 19.11 tes elease ootes
type: docs
weight: 20
url: /ar/java/aspose-3d-for-java-19-11-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for Java 19.11.

{{% /alert %}} 
## **Ements proو Cمعلقة**

|` `**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-575 |` `Add .ATT ملف دعم الاستيراد.|` `New ميزة|
|THREEDNET-578 |` `Add .ATT ملف دعم التصدير|` `New ميزة|
|THREEDNET-577 |` ` Rإيفاكتور و[نظام الملكية](/3d/ar/java/read-3d-document/#read3ddocument-workingwith3dproperties)في Aspose.3D|` `Enhancement|
|THREEDNET-583 |` ` غير مدعوم[RVM نوع الكيان](/3d/ar/java/specify-3d-file-save-options/#specify3dfilesaveoptions-useofrvmsaveoptions) |` `Enhancement|
|THREEDNET-580 |` `[FBX Import](/3d/ar/java/specify-3d-file-load-options/#specify3dfileloadoptions-usefbxloadoptions)Xcاكسيبتيون|` `Enhancement|
|THREEDNET-579 |` ` roroblem مع RVM إلى GLTF تحويل|` `Bug|
|THREEDNET-582 |` ` roroblem مع RVM التحويل|` `Bug|
|THREEDNET-585 |` ` ixixed أخطاء التحقق من صحة الملفات التي تم إنشاؤها glTF|` `Bug|
## **API التغييرات**
### **Added فئة com.aspose.threed. ptions ptions ptions ptions oadO**
When بعض الخصائص المحددة في أقسام الإعداد العالمي 07610348 لديها بديل مماثل في Aspose.ThreeD. sssetInfo ، سيتم استهلاكها وتحويلها إلى الممتلكات الأصلية ، وبالتالي لا يمكنك الوصول إليها من خلال الملكية الديناميكية.

In Aspose.3D 19.11 ، يمكنك استخدام eepBuiltinGlobalSettings في ptions ptions ptions ptions oadOالوصفات لإيقاف هذه الميزة ، والحفاظ على كل شيء في elobalSettings غير مصفاة.

**Sرمز وافرة:**

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
### **Added فئة com.aspose.threed.RvmFormat**
### **Dإفينيتيون:**
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

Tله يسمح للمستخدم لتحميل يدويا. Att ملف وإرفاق البيانات الوصفية إلى مثيل مشهد محدد ، مفيدة عند. لا يمكن العثور على ملف att من قبل Aspose.3D.

Sرمز وافرة:

{{% alert color="primary" %}} 

Scene المشهد = جديد cencene (@ "هذا المجلد \ test.rvm") ؛
OrileFormat.RVM _ BINRY. loadAttributes (المشهد ، @ "هذا المجلد \ اختبار. att") ؛

{{% /alert %}} 
### **أعضاء Added إلى فئة com.aspose.threed. ptions vmLoadOالوصفات**
{{% alert color="primary" %}} 

/**
\ * Gets بادئة الصفات التي تم تحديدها في ملفات السمة الخارجية ،
\ * Tيتم استخدام بادئة لتجنب صراعات الاسم ، القيمة الافتراضية هي "rvm:"
*/
العامة trtring getAttributePإصلاح () ؛

/**
\ * Sets بادئة الصفات التي تم تحديدها في ملفات السمة الخارجية ،
\ * Tيتم استخدام بادئة لتجنب صراعات الاسم ، القيمة الافتراضية هي "rvm:"
\ * @ Param قيمة New قيمة
*/
الفراغ العام setAttributePالإصلاح (قيمة tring S) ؛

خاص attributring السمة إعادة الإصلاح.
/**
\ * Gets سواء لتحميل سمات من ملف قائمة السمة الخارجية (.att/.attrib/.txt) ، القيمة الافتراضية صحيحة.
*/
العامة boolean getLookupAttributes() ؛

/**
\ * Sets سواء لتحميل سمات من ملف قائمة السمة الخارجية (.att/.attrib/.txt) ، القيمة الافتراضية صحيحة.
\ * @ Param قيمة New قيمة
*/
الفراغ العام setLookupAttributes (قيمة منطقية) ؛

{{% /alert %}} 
### **أعضاء Added إلى الفئة com.aspose.threed. ptions vmSaveOptions**
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



**Sوافرة Code**

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
### **Property dded الملكية roroperties إلى الفئة com.aspose.threed.A3 Db**
{{< highlight "java" >}}

     /**

     * Gets the collection of all properties.

     */

    public PropertyCollection getProperties();

{{< /highlight >}}
### **Added فئة com.aspose.threed.**
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

**Sوافرة Code**

{{< highlight "java" >}}

مشهد cencene = جديد cencene ("Camera.fbx") ؛

المواد المادية = المشهد. getRootNode().getChildNodes().get(0).getMaterial() ؛

PropertyCالدعائم ollection = material.getProperties() ؛

// Ist ist جميع الخصائص باستخدام لكل

ل (Pروبيرتي الدعامة: الدعائم)

            {

Prinyالجذعية. out.printf("٪ s = ٪ s \ n" ، الدعامة. getName() ، الدعامة. getValue() ؛

}

// أو استخدام المرسوم للحلقة

ل (int i = 0; i< props.size(); i++)

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
