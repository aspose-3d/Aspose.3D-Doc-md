---
title: Aspose.3D for Java 19,7 Utgivning
type: docs
weight: 60
url: /sv/java/aspose-3d-for-java-19-7-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 19,7](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.7)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-449|Problem med transformationsvärden i Noder|Funktion|
|THREEDNET-526|Lägg till punkt moln exportstöd Google Draco|Förbättring|
|THREEDNET-524|Lägg till stöd för molnimport i Google Draco|Förbättring|
|THREEDNET-523 |Lägg till stöd för punkt moln i PLY format|Förbättring|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **Lagt till ny klass com.aspose.3reed.PointCloud.**
Denna klass ärver från Aspose.ThreeD.Enheter.Geometri direkt och används för att representera en uppsättning poäng.
### **Lagt till nya metoder avkoda till klass com.aspose.treed.DracoFormatt**
{{< highlight "java" >}}

  	/**

     * Decode the point cloud or mesh from specified file name

     * @param fileName The file name contains the drc file

     * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance depends on the file content

     */

    public Geometry decode(String fileName)

        throws ImportException;

    /**

     * Decode the point cloud or mesh from memory data

     * @param data The raw drc bytes

     * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance depends on the content

     */

    public Geometry decode(byte[]data)

        throws ImportException;

{{< /highlight >}}

Provkod för att avkoda en mesh från en draco-fil direkt utan att bygga en scen.

{{< highlight "java" >}}

 PointCloud pointCloud = (PointCloud)FileFormat.DRACO.decode("pointCloud.drc");

{{< /highlight >}}
### **Lagt till nya metoder koda till klass com.aspose.treed.DracoFormatt**
{{< highlight "java" >}}

  /**

     * Encode the entity to specified stream

     * @param entity The entity to be encoded

     * @param stream The stream that encoded data will be written to

     * @param options Extra options for encoding the point cloud

     */

    public void encode(Entity entity, Stream stream, DracoSaveOptions options)

        throws IOException;

    /**

     * Encode the entity to specified stream

     * @param entity The entity to be encoded

     * @param stream The stream that encoded data will be written to

     */

    public void encode(Entity entity, Stream stream)

        throws IOException;


    /**

     * Encode the entity to specified file

     * @param entity The entity to be encoded

     * @param fileName The file name to be written

     */

    public void encode(Entity entity, String fileName)

        throws IOException;

    /**

     * Encode the entity to Draco raw data

     * @param entity The entity to be encoded

     * @param options Extra options for encoding the point cloud

     * @return The encoded draco data represented in bytes

     */

    public byte[]encode(Entity entity, DracoSaveOptions options);

    /**

     * Encode the entity to Draco raw data

     * @param entity The entity to be encoded

     * @return The encoded draco data represented in bytes

     */

    public byte[]encode(Entity entity);

{{< /highlight >}}

Provkod för att koda ett sfärsnät till draco-fil direkt utan att bygga en scenn

{{< highlight "java" >}}

 FileFormat.DRACO.encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
### **Tillagd ny getter/setter getPointCloud/setPointCloud till klass com.aspose.treed.DracoSaveOptioner**


{{< highlight "java" >}}

 /**

 * Export the scene as point cloud, default value is false.

 */

public boolean getPointCloud();

/**

 * Export the scene as point cloud, default value is false.

 * @param value New value

 */

public void setPointCloud(boolean value);

{{< /highlight >}}

Provkod för att koda ett sfärsnät till draco-filen som ett punktmoln

{{< highlight "java" >}}

 DracoSaveOptions opt = new DracoSaveOptions();

opt.setPointCloud(true);

FileFormat.DRACO.encode(new Sphere(), "sphere.drc", opt);

{{< /highlight >}}
### **Lagt till nya metoder koda till klass com.aspose.3reed.PlyFormat.**
{{< highlight "java" >}}

 /**

 * Encode the entity and save the result into the stream.

 * @param entity The entity to encode

 * @param stream The stream to write to, this method will not close this stream

 * @param opt Save options

 */

public void encode(Entity entity, Stream stream, PlySaveOptions opt)

    throws IOException;

/**

 * Encode the entity and save the result into the stream.

 * @param entity The entity to encode

 * @param stream The stream to write to, this method will not close this stream

 */

public void encode(Entity entity, Stream stream)

    throws IOException;

/**

 * Encode the entity and save the result into an external file.

 * @param entity The entity to encode

 * @param fileName The file to write to

 * @param opt Save options

 */

public void encode(Entity entity, String fileName, PlySaveOptions opt)

    throws IOException;

/**

 * Encode the entity and save the result into an external file.

 * @param entity The entity to encode

 * @param fileName The file to write to

 */

public void encode(Entity entity, String fileName)

    throws IOException;

{{< /highlight >}}

Provkod för att koda en mesh för att ply filen direkt utan att bygga en scen.

{{< highlight "java" >}}

 FileFormat.PLY.encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
### **Lagt till nya metoder avkoda till klass com.aspose.3reed.PlyFormat.**
{{< highlight "java" >}}

 /**

 * Decode a point cloud or mesh from the specified stream.

 * @param fileName The input stream

 * @param opt The load option of PLY format

 * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance

 */

public Geometry decode(String fileName, PlyLoadOptions opt)

    throws IOException;

/**

 * Decode a point cloud or mesh from the specified stream.

 * @param fileName The input stream

 * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance

 */

public Geometry decode(String fileName)

    throws IOException;

/**

 * Decode a point cloud or mesh from the specified stream.

 * @param stream The input stream

 * @param opt The load option of PLY format

 * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance

 */

public Geometry decode(Stream stream, PlyLoadOptions opt)

    throws IOException;

/**

 * Decode a point cloud or mesh from the specified stream.

 * @param stream The input stream

 * @return A {@link com.aspose.threed.Mesh} or {@link com.aspose.threed.PointCloud} instance

 */

public Geometry decode(Stream stream)

    throws IOException;

{{< /highlight >}}

Provkod för att avkoda ett nät/punktmoln från en lagfil:

{{< highlight "java" >}}

 Geometry geom = FileFormat.PLY.decode("sphere.ply");

{{< /highlight >}}
### **Tillägg getter/setter getPointCloud och setPointCloud till klass com.aspose.treed.PlySaveOptioner**
{{< highlight "java" >}}

 /**

 * Export the scene as point cloud, the default value is false.

 */

public boolean getPointCloud();

/**

 * Export the scene as point cloud, the default value is false.

 * @param value New value

 */

public void setPointCloud(boolean value);

{{< /highlight >}}

Samplingskod för att tvinga att exportera en scen att spela som punktmoln

{{< highlight "java" >}}

 PlySaveOptions opt = new PlySaveOptions();

opt.setPointCloud(true);

FileFormat.PLY.encode(new Sphere(), "sphere.ply", opt);

{{< /highlight >}}
