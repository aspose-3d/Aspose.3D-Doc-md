+++
title = "Aspose.3D for Java 18.9 - September 2018" 
description = "" 
weight = 12077 
+++

Aspose.3D for Java : Aspose.3D for Java 18.9 - September 2018  

# Aspose.3D for Java : Aspose.3D for Java 18.9 - September 2018


This page contains release notes for [Aspose.3D for Java 18.9](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.9/).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Summary|Category|
|:----|:----|
|CancellationToken support|New Feature|
|FBX ExportException - High Polygon Count|Bug|
|ImportException while opening huge FBX files|Bug|
|Not all properties from FBX's global settings are loaded into the AssetInfo|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

Please view the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java API. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### API changes:

#### Class com.aspose.threed.Node added 2 new methods:

{{< code lang="cs" >}}
    /**
     * Per-node asset info
     * @param value New value
     */
    public void setAssetInfo(com.aspose.threed.AssetInfo);
    /**
     * Per-node asset info
     */
    public com.aspose.threed.AssetInfo getAssetInfo();
{{< /code >}}

  
Some file types can have per-node's asset information.  
In FBX, the AssetInfo property of root node contains the global settings defined in FBX files.

**Sample Code:**

{{< code lang="cs" >}}
        //Access GlobalSettings in FBX file, more properties can be found by opening the ASCII FBX files in a text editor.
        //And FBXHeaderExtension/SceneInfo inside FBX file will be mapped to Scene.AssetInfo
        Scene scene = new Scene("test.fbx");
        AssetInfo globalSettings = scene.getRootNode().getAssetInfo();
        System.out.println(globalSettings.getProperty("DefaultCamera"));
        System.out.println(globalSettings.getProperty("UpAxis"));
        System.out.println(globalSettings.getProperty("FrontAxis"));
{{< /code >}}

#### Class com.aspose.threed.Scene added 10 new methods:

These are all new overloads to the original save/open methods:

**Old Methods:**

{{< code lang="cs" >}}
    /**
     * Opens the scene from given stream using specified file format.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param format File format.
     * @param cancellationToken Cancellation token to the load task
     */
    public void open(Stream stream, FileFormat format, Cancellation cancellationToken)
        throws ImportException;
    /**
     * Opens the scene from given stream using specified IO config.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param options More detailed configuration to open the stream.
     * @param cancellationToken Cancellation token to the load task
     */
    public void open(Stream stream, LoadOptions options, Cancellation cancellationToken)
        throws ImportException;
    /**
     * Opens the scene from given stream
     * @param stream Input stream, user is responsible for closing the stream.
     * @param cancellationToken Cancellation token to the load task
     */
    public void open(Stream stream, Cancellation cancellationToken)
        throws IOException;
    /**
     * Opens the scene from given path using specified file format.
     * @param fileName File name.
     * @param format File format.
     * @param cancellationToken Cancellation token to the load task
     */
    public void open(String fileName, FileFormat format, Cancellation cancellationToken)
        throws IOException;
    /**
     * Opens the scene from given path using specified file format.
     * @param fileName File name.
     * @param options More detailed configuration to open the stream.
     * @param cancellationToken Cancellation token to the load task
     */
    public void open(String fileName, LoadOptions options, Cancellation cancellationToken)
        throws IOException;
    /**
     * Opens the scene from given path
     * @param fileName File name.
     * @param cancellationToken Cancellation token to the load task
     */
    public void open(String fileName, Cancellation cancellationToken)
        throws IOException;
    /**
     * Saves the scene to stream using specified file format.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param format Format.
     * @param cancellationToken Cancellation token to the save task
     */
    public void save(Stream stream, FileFormat format, Cancellation cancellationToken)
        throws ExportException;
    /**
     * Saves the scene to stream using specified file format.
     * @param stream Input stream, user is responsible for closing the stream.
     * @param options More detailed configuration to save the stream.
     * @param cancellationToken Cancellation token to the save task
     */
    public void save(Stream stream, SaveOptions options, Cancellation cancellationToken)
        throws ExportException;
    /**
     * Saves the scene to specified path using specified file format.
     * @param fileName File name.
     * @param format Format.
     * @param cancellationToken Cancellation token to the save task
     */
    public void save(String fileName, FileFormat format, Cancellation cancellationToken)
        throws IOException;
    /**
     * Saves the scene to specified path using specified file format.
     * @param fileName File name.
     * @param options More detailed configuration to save the stream.
     * @param cancellationToken Cancellation token to the save task
     */
    public void save(String fileName, SaveOptions options, Cancellation cancellationToken)
        throws IOException;
{{< /code >}}

You can use the Cancellation to cancel the save/open task at any time you need.  

**Sample Code:**

{{< code lang="cs" >}}
        final Cancellation cts = new Cancellation();
        Thread thread = new Thread(() -> {
            try {
                Thread.sleep(1000);
                cts.cancel();
            } catch(InterruptedException e) {
                throw new RuntimeException(e);
            }
        });
        thread.start();
        Scene scene = new Scene();
        try {
            scene.open("test.fbx", cts);
            System.out.println("Import is done within 1000ms");
        } catch(ImportException e) {
            if(e.getCause() instanceof CancellationException) {
                System.out.println("It takes too long time to import, and we have canceled the importing.");
            }
        }
{{< /code >}}

  

