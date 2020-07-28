+++
title = "Aspose.3D for Java 19.5 Release Notes" 
description = "" 
weight = 12068 
+++

Aspose.3D for Java : Aspose.3D for Java 19.5 Release Notes  

# Aspose.3D for Java : Aspose.3D for Java 19.5 Release Notes


This page contains release notes for [Aspose.3D for Java 19.5](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.5)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-501|Integrate with latest Dynabic.Metered|Enhancement|
|THREEDNET-505|Allow change plane's orientation by specifying an up normal|Enhancement|
|THREEDNET-489|Shadow is not working in Vulkan renderer|Bug|
|THREEDNET-504|Draco created from STL file is broken|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

#### Added new property \*Radius\* in class com.aspose.threed.Plane

{{< code lang="cs" >}}
/**
 * Gets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane
 */
public Vector3 getUp();
/**
 * Sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane
 * @param value New value
 */
public void setUp(Vector3 value);
{{< /code >}}

Sample code to specify radius by property rather than constructor argument:

{{< code lang="cs" >}}
Scene scene = new Scene();
Plane plane = new Plane();
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save("test.obj", FileFormat.WAVEFRONTOBJ);
{{< /code >}}

#### Added new method "getConsumptionCredit" in class com.aspose.threed.Metered

{{< code lang="cs" >}}
/**
* Gets consumption credit
* @return consumption quantity
*/
public static double getConsumptionCredit() throws Exception;
{{< /code >}}

Gets the consumption credit of current month, used by Dynabic.Metered billing service.

