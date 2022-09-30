---
title: Aspose.3D for Java 19,10 Utgivningsmeddelanden
type: docs
weight: 30
url: /sv/java/aspose-3d-for-java-19-10-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 19,0](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.10).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-567 |` `Problem konvertering RVM & ATT bricka|` `Förbättring|
|THREEDNET-570 |` `Beräkning av avgränsande låda av primitiva former är felaktig|` `Förbättring|
|THREEDNET-571 |` `Export primitiva former till RVM fil.|` `Förbättring|
|THREEDNET-572 |` `Förbättra det primitiva exportstödet under FBX.|` `Förbättring|
|THREEDNET-573 |` `Speciella tecken i objektnamn kan inte exporteras korrekt i FBX format.|` `Bug|
|THREEDNET-568 |` ` Sparat. Gb- filer kan inte öppnas.|` `Bug|
|THREEDNET-549|Att lasta enorm RVM tar mycket tid och resurser|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **Ny klass - com.aspose. Threed.Dish**
Detta är en ny parameteriserad primitiv form.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish", new Dish(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **Ny klass - com.aspose. Threed.Pyramid**
Detta är en ny parameteriserad primitiv form.

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("pyramid", new Pyramid(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **Nya egenskaper lagts till i klassen com.aspose.3reed.Box**


Följande egenskaper har lagts till i Aspose.ThreeD Enheter.Box-klass.

{{< highlight "java" >}}

 /**

\* Gets the length segments.

*/

public int getLengthSegments();

/**

\* Sets the length segments.

\* @param value New value

*/

public void setLengthSegments(int value);

/**

\* Gets the width segments

*/

public int getWidthSegments();

/**

\* Sets the width segments

\* @param value New value

*/

public void setWidthSegments(int value);

/**

\* gets or sets the height segments.

*/

public int getHeightSegments();

/**

\* gets or sets the height segments.

\* @param value New value

*/

public void setHeightSegments(int value);

{{< /highlight >}}
### **Avlägsnad metod HittaNode i klass com.aspose.3reed.Node.**
Detta var planerat att tas bort eftersom det har ersatts av mer avancerade SelectSingleObject/Select Objekt.
### **Ny metod läggs till klass com.aspose.3reed.Node.**
Följande metod har lagts till Aspose.ThreeD.Nod klass som gör det mer bekvämt att skapa en nod med en Material.

{{< highlight "java" >}}

 /**

\* Create a new child node with given node name, and attach specified entity and a material

\* @param nodeName The new child node's name

\* @param entity Default entity attached to the node

\* @param material The material attached to the node

\* @return The new child node.

*/

public Node createChildNode(String nodeName, Entity entity, Material material);

{{< /highlight >}}

Urvalskod

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish", new Box(), new PbrMaterial(Color.blue));

{{< /highlight >}}
### **Avlägsnade metoder från klass com.aspose.3reed.PlyFormat.**


Följande metoder har ersatts av PlyFormat.Encode som också kan användas för att koda punktmoln.



{{< highlight "java" >}}

 private void encodeMesh(IMeshConvertible mesh, Stream stream, PlySaveOptions opt) throws IOException;

private void encodeMesh(IMeshConvertible mesh, String fileName, PlySaveOptions opt) throws IOException;

{{< /highlight >}}
### **Lagt ny egenskap till klassen com.aspose.treed.FBXSaveOptions.**
Denna egenskap gör det praktiskt att exportera stora scener som består av primitiva.



{{< highlight "java" >}}

 /**

 * Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

\* Default value is false

*/

public boolean getReusePrimitiveMesh();



/**

\* Reuse the mesh for the primitives with same parameters, this will significantly reduce the size of FBX output which scene was constructed by large set of primitive shapes(like imported from CAD files).

\* Default value is false

\* @param value New value

*/

public void setReusePrimitiveMesh(boolean value);

{{< /highlight >}}
#### **Urvalskod**
{{< highlight "java" >}}

 Scene scene = new Scene();

scene.getRootNode().createChildNode("dish A", new Dish(), new PbrMaterial(Color.blue));

scene.getRootNode().createChildNode("dish B", new Dish(), new PbrMaterial(Color.blue));

FBXSaveOptions opt = new FBXSaveOptions(FileFormat.FBX7400ASCII);

opt.setReusePrimitiveMesh(true);

scene.save("file.fbx", opt);

{{< /highlight >}}



Eftersom de två parameteriserade formerna har samma parametrar, kommer de definitivt generera samma mesh. När denna egenskap är sann, kommer den genererade FBX filen bara generera en mesh och återanvända den i olika noder.
