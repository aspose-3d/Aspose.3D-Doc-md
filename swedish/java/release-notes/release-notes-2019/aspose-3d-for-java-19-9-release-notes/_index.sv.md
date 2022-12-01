---
title: Aspose.3D for Java 19,9 Utgivning
type: docs
weight: 40
url: /sv/java/aspose-3d-for-java-19-9-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller publiceringsanmärkningar för Aspose.3D for Java 19,9

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-532|Export 3D scen till HTML|Ny funktion|
|THREEDNET-561|Exponera geometriska transformationsegenskaper|Förbättring|
|THREEDNET-556|Geometrisk rotation verkar felaktig|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **Lagt till nya filformat HTML5/ASPOSE3D_WEB**
{{< highlight "java" >}}

 /**

\* Aspose.3D Web format.

*/

public static final FileFormat ASPOSE3D_WEB;

/**

\* HTML5 File

*/

public static final FileFormat HTML5;

{{< /highlight >}}

När du exporterar scenen till HTML5 fil, kommer det att finnas faktiskt 3 filer, en HTML fil, en Aspose3DWeb-fil(*. a3dw), och en uppvisad JavaScript- fil, du kan bara exportera a3dw-filen genom att ange Aspose3DWeb som exporttyp, och återanvänd javascript-filen inom din egen HTML sida.

Provkod:

{{< highlight "java" >}}

 Scene scene = new Scene();

Node node = scene.getRootNode().createChildNode(new Cylinder());

LambertMaterial mat = new LambertMaterial();

mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));

node.setMaterial(mat);

Light light = new Light();

light.setLightType(LightType.POINT);

scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);

scene.save("test.html", FileFormat.HTML5);

{{< /highlight >}}

{{% alert color="primary" %}} 

På grund av webbläsarens säkerhetsgränser kan den exporterade HTML-filen inte öppnas direkt, du måste öppna den via en webbserver, om du har python3 installerad, kan du starta webbservern i kommandoraden i den exporterade katalogen

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Öppna den då.**Http://localhost:8000/test.html.**. Webbens återgivning använder WebGL2, som du kan använda.<https://get.webgl.org/webgl2/>För att kontrollera om din webbläsare stöder det eller inte.
### **Lagt till ny klass com.aspose.3reed.HTML5SaveOptions.**
Detta gör att du kan anpassa den exporterade 3D HTML sida

Provkod:

{{< highlight "java" >}}

 Scene scene = new Scene();

Node node = scene.getRootNode().createChildNode(new Cylinder());

LambertMaterial mat = new LambertMaterial();

mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));

node.setMaterial(mat);

Light light = new Light();

light.setLightType(LightType.POINT);

scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);

HTML5SaveOptions opt = new HTML5SaveOptions();

opt.setShowGrid(false); // Turn off the grid

opt.setShowUI(false); //Turn off the user interface

scene.save("test.html", FileFormat.HTML5);

{{< /highlight >}}
### **Tillagd ny egenskap FileFormat i klass com.aspose.3reed.IOConfig**
{{< highlight "java" >}}

 /**

 * Gets the file format that specified in current Save/Load option.

 */

public FileFormat getFileFormat();

{{< /highlight >}}
### **Tillagd ny metod utvärderaGlobalTransform i klass com.aspose.3reed.Node.**
{{< highlight "java" >}}

 /**

 * Evaluate the global transform, include the geometric transform or not.

 * @param withGeometricTransform Whether the geometric transform is needed.

 */

public Matrix4 evaluateGlobalTransform(boolean withGeometricTransform);

{{< /highlight >}}

Skillnaden mellan Node. GlobalTransform. TransformMatrix är att det låter dig få en transformationsmatris med en geometrisk transformation, som endast påverkar den bifogade enheten och håller barnnoderna opåverkade.
### **Tillagd ny getter/setGeometricÖversättning/setGeometricÖversättning/gge cScaling/getGeometricRotation/setGeometricRotation i klass com. Förmodligen. Tre. Transforma**


{{< highlight "java" >}}

 /**

 * Gets the geometric translation.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 */

public Vector3 getGeometricTranslation();

/**

 * Sets the geometric translation.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 * @param value New value

 */

public void setGeometricTranslation(Vector3 value);

/**

 * Gets the geometric scaling.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 */

public Vector3 getGeometricScaling();

/**

 * Sets the geometric scaling.

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 * @param value New value

 */

public void setGeometricScaling(Vector3 value);

/**

 * Gets the geometric euler rotation(measured in degree).

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 */

public Vector3 getGeometricRotation();

/**

 * Sets the geometric euler rotation(measured in degree).

 * Geometric transformation only affects the entities attached and leave the child nodes unaffected.

 * It will be merged as local transformation when you export the geometric transformation to file types that does not support it.

 * @param value New value

 */

public void setGeometricRotation(Vector3 value);

{{< /highlight >}}



Provkod:

{{< highlight "java" >}}

 Node n = new Node();

n.getTransform().setGeometricTranslation(new Vector3(10, 0, 0));

System.out.println(n.evaluateGlobalTransform(true));

System.out.println(n.evaluateGlobalTransform(false));

{{< /highlight >}}

Den första utskriften kommer att lämna ut transformationsmatrisen som inkluderar den geometriska transformationen medan den andra inte gör det.
