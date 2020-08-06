---
title : "Aspose.3D for Java 19.6 Release Notes" 
description : "" 
weight : 12067 
toc : false
type: docs
url: /java/releasenotes/2019/aspose.3d+for+java+19.6+release+notes/
---

# Aspose.3D for Java : Aspose.3D for Java 19.6 Release Notes


This page contains release notes for [Aspose.3D for Java 19.6](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d/19.6)

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-511|Enhance the creation of cylinder|New Feature|
|THREEDNET-507|Lose some materials while opening the RVM file|Bug|
|THREEDNET-508|The system may fail to allocate descriptor set sometimes in Vulkan renderer|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

#### Added new property OffsetTop in class com.aspose.threed.Cylinder

{{< code lang="cs" >}}
/**
 * Gets the vertices transformation offset of the top side.
 */
public Vector3 getOffsetTop();
/**
 * Sets the vertices transformation offset of the top side.
 * @param value New value
 */
public void setOffsetTop(Vector3 value);
{{< /code >}}

#### Added new property OffsetBorrom in class com.aspose.threed.Cylinder

{{< code lang="cs" >}}
/**
 * Gets the vertices transformation offset of the bottom side.
 */
public Vector3 getOffsetBottom();
/**
 * Sets the vertices transformation offset of the bottom side.
 * @param value New value
 */
public void setOffsetBottom(Vector3 value);
{{< /code >}}

Sample code to generate a cylinder with customized OffsetTop:

{{< code lang="cs" >}}
Scene scene = new Scene();
Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);
cylinder1.setOffsetTop(new Vector3(5, 3, 0));
scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);
Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);
scene.getRootNode().createChildNode(cylinder2);
scene.save("test.obj", FileFormat.WAVEFRONTOBJ);
{{< /code >}}

Preview:

![image](90112037.png)

The left one has **OffsetTop** set to (5, 3, 0), it's easy to see the top cap has moved and the whole torso also gets affected.

#### Added new property GenerateFanCylinder in class com.aspose.threed.Cylinder

{{< code lang="cs" >}}
/**
 * Gets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.
 */
public boolean getGenerateFanCylinder();
/**
 * Sets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.
 * @param value New value
 */
public void setGenerateFanCylinder(boolean value);
{{< /code >}}

Sample code to generate a fan style cylinder and non-fan style cylinder:

{{< code lang="cs" >}}
Scene scene = new Scene();
Cylinder fan = new Cylinder(2, 2, 10, 20, 1, false);
fan.setGenerateFanCylinder(true);
fan.setThetaLength(MathUtils.toRadian(270.0));
scene.getRootNode().createChildNode(fan).getTransform().setTranslation(10, 0, 0);
Cylinder nonfan = new Cylinder(2, 2, 10, 20, 1, false);
scene.getRootNode().createChildNode(nonfan);
scene.save("test.obj", FileFormat.WAVEFRONTOBJ);
{{< /code >}}

Preview:

![image](90112038.png)

The left cylinder has GenerateFanCylinder = false and the right one has GenerateFanCylinder = true.

#### Added new property ShearTop in class com.aspose.threed.Cylinder

\*\* \* Gets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0) \*/public Vector2 getShearTop();/\*\* \* Sets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0) \* @param value New value \*/public void setShearTop(Vector2 value)

#### Added new property ShearBottom in class com.aspose.threed.Cylinder

/\*\* \* Gets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0) \*/public Vector2 getShearBottom();/\*\* \* Sets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0) \* @param value New value \*/public void setShearBottom(Vector2 value);

Sample code to show the usage of ShearBottom(ShearTop):

Scene scene = new Scene();Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);cylinder1.setShearBottom(new Vector2(0, 0.83));//shear 47.5deg in xy plane(z-axis)scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);scene.getRootNode().createChildNode(cylinder2);scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

Preview:

![image](90112039.png)

The left cylinder has ShearBottom to (0, 0.83) while the right one is an ordinal cylinder.

