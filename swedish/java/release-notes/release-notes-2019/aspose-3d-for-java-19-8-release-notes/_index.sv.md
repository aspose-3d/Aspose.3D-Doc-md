---
title: Aspose.3D for Java 19,8 Utgivning
type: docs
weight: 50
url: /sv/java/aspose-3d-for-java-19-8-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 19,8](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.8)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-528|Lägg till stöd för punkt moln i Wavefront OBJ|Ny funktion|
|THREEDNET-531|Säkerhetsgranskning av Aspose.3D|Förbättring|
|THREEDNET-536 |DRC till STL omvandling|FelComment|
|THREEDNET-537|Problem att konvertera PLY till GLB|FelComment|
|THREEDNET-539|Det stora punktmolnet kan generera felaktiga data.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **Lagt till ny getter/setter PointCloud i klassen com.aspose.treed.ObjSaveOptions.**
{{< highlight "java" >}}

 /**

 * Gets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

 */

public boolean getPointCloud();

/**

 * Sets the flag whether the exporter should export the scene as point cloud(without topological structure), default value is false

 * @param value New value

 */

public void setPointCloud(boolean value);

{{< /highlight >}}

Provkod för att skapa ett punktmoln i Sphere i obj format.

{{< highlight "java" >}}

 Scene scene = new Scene(new Sphere());

ObjSaveOptions opt = new ObjSaveOptions();

opt.setPointCloud(true);

scene.save("sphere.obj", opt);

{{< /highlight >}}
### **Lagt till nya metoder skapaPolygon com.aspose.tre.Mesh**
{{< highlight "java" >}}

 /**

 * Create a polygon with 4 vertices(quad)

 * @param v1 Index of the first vertex

 * @param v2 Index of the second vertex

 * @param v3 Index of the third vertex

 * @param v4 Index of the fourth vertex

 */

public void createPolygon(int v1, int v2, int v3, int v4);

/**

 * Create a polygon with 3 vertices(triangle)

 * @param v1 Index of the first vertex

 * @param v2 Index of the second vertex

 * @param v3 Index of the third vertex

 */

public void createPolygon(int v1, int v2, int v3);

{{< /highlight >}}

Provkod.

{{< highlight "java" >}}

 Mesh mesh = new Mesh();

mesh.createPolygon(new int[]{ 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices

mesh.createPolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

{{< /highlight >}}

De nya metoderna**CreatePolygonName**Låter dig skapa en triangel eller quad utan att tilldela extra minne, det är mycket optimerat internt.


### **Ta bort gammalt offentligt fält prettyPrint i klass com.aspose.3reed.GLTFSaveOptioner**
Detta togs bort och ersattes av egendom med samma namn.
### **Lagt till ny getter/setter PrettyPrint i klass com.aspose.treed.GLTFSaveOptions.**
{{< highlight "java" >}}

 /**

\* The JSON content of GLTF file is indented for human reading, default value is false

*/

public boolean getPrettyPrint();

/**

\* The JSON content of GLTF file is indented for human reading, default value is false

\* @param value New value

*/

public void setPrettyPrint(boolean value);

{{< /highlight >}}

Den gamla.**PrettyPrint**Det var ett offentligt fält, och det har ersatts av egendom för konsekvent.

Provkod.

{{< highlight "java" >}}

 Scene scene = new Scene(new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//opt.prettyPrint = true; //Old code

opt.setPrettyPrint(true); //Use setter to change this configuration.

scene.save("sphere.gltf", opt);

{{< /highlight >}}




