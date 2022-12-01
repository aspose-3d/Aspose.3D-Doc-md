---
title: Aspose.3D for Java 22,3 Utgivning
type: docs
weight: 10
url: /sv/java/aspose-3d-for-java-22-3-release-notes/
description: Publiceringsnoterna av Aspose.3D for Java 22.3.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 22.3.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1103 |Förbättra stora mesh till U3D/PDF fil exportering|Förbättring|
|THREEDNET-1081 |Lägg till förenklade funktioner för att sammanfoga scener|Förbättring|
|THREEDNET-1077 |Genererad glTF kan inte passera glTF validator när draco komprimering aktiverad.|Felrättning|


## API ändringar ##


### Lagt till nya statiska metoder till klass `com.aspose.threed.Scene`:

{{< highlight "java" >}}
    /**
     * Opens the scene from given stream using specified file format.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param format File format.
     * @param cancellationToken Cancellation token to the load task
     */
    public static Scene fromStream(Stream stream, FileFormat format, Cancellation cancellationToken) throws IOException;
    /**
     * Opens the scene from given stream using specified file format.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param format File format.
     */
    public static Scene fromStream(Stream stream, FileFormat format) throws IOException;
    /**
     * Opens the scene from given stream using specified IO config.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param options More detailed configuration to open the stream.
     * @param cancellationToken Cancellation token to the load task
     */
    public static Scene fromStream(Stream stream, LoadOptions options, Cancellation cancellationToken) throws IOException;
    /**
     * Opens the scene from given stream using specified IO config.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param options More detailed configuration to open the stream.
     */
    public static Scene fromStream(Stream stream, LoadOptions options) throws IOException;
    /**
     * Opens the scene from given stream
     * @param stream Input stream, user is responsible for closing the stream.
     * @param cancellationToken Cancellation token to the load task
     */
    public static Scene fromStream(Stream stream, Cancellation cancellationToken) throws IOException;
    /**
     * Opens the scene from given stream
     * @param stream Input stream, user is responsible for closing the stream.
     */
    public static Scene fromStream(Stream stream) throws IOException;
{{< /highlight >}}

Dessa överbelastningar gör det möjligt att konstruera en scen direkt från en ström, med fler alternativ ärvt från Scene.

{{< highlight "java" >}}
        //Before 22.3, load a scene from stream:
        //var scene = new Scene();
        //scene.open(stream);

        //Now we load a scene from stream
        var scene = Scene.fromStream(stream);
{{< /highlight >}}


### Lagt till nya statiska metoder till klass `com.aspose.threed.Scene`:

{{< highlight "java" >}}
    /**
     * Opens the scene from given path using specified file format.
     * @param fileName File name.
     * @param format File format.
     * @param cancellationToken Cancellation token to the load task
     */
    public static Scene fromFile(String fileName, FileFormat format, Cancellation cancellationToken) throws IOException;
    /**
     * Opens the scene from given path using specified file format.
     * @param fileName File name.
     * @param format File format.
     */
    public static Scene fromFile(String fileName, FileFormat format) throws IOException;

    /**
     * Opens the scene from given path using specified file format.
     * @param fileName File name.
     * @param options More detailed configuration to open the stream.
     * @param cancellationToken Cancellation token to the load task
     */
    public static Scene fromFile(String fileName, LoadOptions options, Cancellation cancellationToken) throws IOException;

    /**
     * Opens the scene from given path using specified file format.
     * @param fileName File name.
     * @param options More detailed configuration to open the stream.
     */
    public static Scene fromFile(String fileName, LoadOptions options) throws IOException;

    /**
     * Opens the scene from given path
     * @param fileName File name.
     * @param cancellationToken Cancellation token to the load task
     */
    public static Scene fromFile(String fileName, Cancellation cancellationToken) throws IOException;
    /**
     * Opens the scene from given path
     * @param fileName File name.
     */
    public static Scene fromFile(String fileName) throws IOException;
{{< /highlight >}}

Dessa överbelastningar gör det möjligt att konstruera en scen direkt från filnamn, med fler alternativ ärvt från Scene. Öppna.

Den gamla konstruktören av Scene med en filName

{{< highlight "java" >}}
        //Before 22.3, load a scene from file:
        //var scene = new Scene();
        //scene.open("fileName");

        //Now we load a scene from file
        var scene = Scene.fromFile("fileName");
{{< /highlight >}}




### Lagt till nya statiska metoder till klass `aspose.threed.Node`:

{{< highlight "java" >}}
    /**
     * Detach everything under the node and attach them to current node.
     * @param node 
     */
    public void merge(Node node);
{{< /highlight >}}


Denna nya metod tillåter att sammanfoga allt från en annan nod till nuvarande nod.

Samplingskod för att sammanfoga filen1 och filen2:

{{< highlight "java" >}}
        var scene1 = Scene.fromFile("file1");
        var scene2 = Scene.fromFile("file2");
        scene1.getRootNode().merge(scene2.getRootNode());
        scene1.save("output.fbx", FileFormat.FBX7700_BINARY);
{{< /highlight >}}

