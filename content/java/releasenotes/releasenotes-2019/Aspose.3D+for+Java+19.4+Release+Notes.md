+++
title = "Aspose.3D for Java 19.4 Release Notes" 
description = "" 
weight = 12069 
+++

Aspose.3D for Java : Aspose.3D for Java 19.4 Release Notes  

# Aspose.3D for Java : Aspose.3D for Java 19.4 Release Notes


This page contains release notes for [Aspose.3D for Java 19.4](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.4)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-483 |Support for VRML format |New feature|
|THREEDJAVA-26|Rendering support for Aspose.3D for Java |New feature|
|THREEDNET-496 |FBX7500Binary Export Corruption Issue |Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

#### Added new property Radius in class com.aspose.threed.Sphere

{{< code lang="cs" >}}
/**
 * Gets the radius of the sphere.
 */
public double getRadius();
/**
 * Sets the radius of the sphere.
 * @param value New value
 */
public void setRadius(double value);
{{< /code >}}

Sample code to specify radius by property rather than constructor argument:

{{< code lang="cs" >}}
Scene scene = new Scene();
Sphere sphere = new Sphere();
sphere.setRadius(10);
scene.getRootNode().createChildNode(sphere);
scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);
{{< /code >}}

#### Added new file format VRML in class com.aspose.threed.FileFormat and com.aspose.threed.FileFormatType

{{< code lang="cs" >}}
/**
 * The Virtual Reality Modeling Language
 */
public static final FileFormat VRML;
{{< /code >}}

Aspose.3D can auto-detect VRML format, so the FileFormat is usually ignored in the Open method. Sample code:

{{< code lang="cs" >}}
Scene scene = new Scene();
scene.open("test.wrl");
{{< /code >}}

