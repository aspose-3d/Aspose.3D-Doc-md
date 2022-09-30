---
title: Aspose.3D for Java 19.9 Note di rilascio
type: docs
weight: 40
url: /it/java/aspose-3d-for-java-19-9-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per Aspose.3D for Java 19.9

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-532|Esporta la scena 3D allo HTML|Nuova funzione|
|THREEDNET-561|Esporre le proprietà geometriche di trasformazione|Miglioramento|
|THREEDNET-556|La rotazione geometrica sembra errata|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for Java. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **Aggiunti nuovi formati di file HTML5/ASPOSE3D _ WEB**
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

Quando si esporta la scena nel file HTML5, ci saranno in realtà 3 file, un file HTML, un file DWeb Aspose3 (*.a3dw) e un file JavaScript renderizzato, è possibile esportare il file a3dw solo specificando DWeb Aspose3 come tipo di esportazione e riutilizzare il file javascript all'interno della propria pagina HTML.

Codice del campione:

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

A causa dei limiti di sicurezza del browser, il file HTML esportato non può essere aperto direttamente, è necessario aprirlo tramite un server Web, se è installato python3, è possibile avviare il server Web nella riga di comando nella directory esportata

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Allora aprilo**http:// localhost:8000/test.html**. Il renderer web utilizza WebGL2, è possibile utilizzare<https://get.webgl.org/webgl2/>Per verificare se il tuo browser lo supporta o meno.
### **Aggiunta nuova classe com.aspose.threed.HTML5SaveOptions**
Questo permette di personalizzare la pagina 3D esportate HTML

Codice del campione:

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
### **Aggiunta nuova proprietà FileFormat nella classe com.aspose.threed.IOConfig**
{{< highlight "java" >}}

 /**

 * Gets the file format that specified in current Save/Load option.

 */

public FileFormat getFileFormat();

{{< /highlight >}}
### **Aggiunto nuovo metodo di valutazione GlobalTransform in classe com.aspose.threed.Node**
{{< highlight "java" >}}

 /**

 * Evaluate the global transform, include the geometric transform or not.

 * @param withGeometricTransform Whether the geometric transform is needed.

 */

public Matrix4 evaluateGlobalTransform(boolean withGeometricTransform);

{{< /highlight >}}

La differenza tra Node.GlobalTransform.TransformMatrix è che consente di ottenere una matrice di trasformazione con una trasformata geometrica, che influisce solo sull'entità collegata e mantiene inalterati i nodi figlio.
### **Aggiunto nuovo getter/setter getGeometricTranslation/setGeometricTranslation/getGeometricScaling/setGeometricScaling/getGeometricRotation/setGeometricRotation in class com.aspose.threed.Transform**


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



Codice del campione:

{{< highlight "java" >}}

 Node n = new Node();

n.getTransform().setGeometricTranslation(new Vector3(10, 0, 0));

System.out.println(n.evaluateGlobalTransform(true));

System.out.println(n.evaluateGlobalTransform(false));

{{< /highlight >}}

La prima istruzione di stampa emetterà la matrice di trasformazione che include la trasformazione geometrica mentre la seconda no.
