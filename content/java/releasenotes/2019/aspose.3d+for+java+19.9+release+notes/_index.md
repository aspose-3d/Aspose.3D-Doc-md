---
title : "Aspose.3D for Java 19.9 Release Notes" 
description : "" 
weight : 12064 
toc : false
type: docs
url: /java/releasenotes/2019/aspose.3d+for+java+19.9+release+notes/
---

# Aspose.3D for Java : Aspose.3D for Java 19.9 Release Notes


This page contains release notes for Aspose.3D for Java 19.9

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-532|Export 3D scene to HTML|New Feature|
|THREEDNET-561|Expose geometric transformation properties|Enhancement|
|THREEDNET-556|Geometric rotation seems incorrect|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### Added new file formats HTML5/ASPOSE3D\_WEB

{{< code lang="cs" >}}
/**
* Aspose.3D Web format.
*/
public static final FileFormat ASPOSE3D_WEB;
/**
* HTML5 File
*/
public static final FileFormat HTML5;
{{< /code >}}

When you export the scene into HTML5 file, there will be actually 3 files, an HTML file, an Aspose3DWeb file(\*.a3dw), and a rendered JavaScript file, you can only export the a3dw file by specifying the Aspose3DWeb as the export type, and reuse the javascript file within your own HTML page.

Sample code:

{{< code lang="cs" >}}
Scene scene = new Scene();
Node node = scene.getRootNode().createChildNode(new Cylinder());
LambertMaterial mat = new LambertMaterial();
mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));
node.setMaterial(mat);
Light light = new Light();
light.setLightType(LightType.POINT);
scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);
scene.save("test.html", FileFormat.HTML5);
{{< /code >}}

Due to the browser's security limits, the exported HTML file cannot be opened directly, you need to open it through a web server, if you have python3 installed, you can start the webserver in the command line in the exported directory

python3 -m http.server

Then open it [http://localhost:8000/test.html](http://localhost:8000/test.html). The web renderer uses WebGL2, you can use [https://get.webgl.org/webgl2/](https://get.webgl.org/webgl2/) to check if your browser supports it or not.

### Added new class com.aspose.threed.HTML5SaveOptions

This allows you to customize the exported 3D HTML page

Sample code:

Scene scene = new Scene();Node node = scene.getRootNode().createChildNode(new Cylinder());LambertMaterial mat = new LambertMaterial();mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));node.setMaterial(mat);Light light = new Light();light.setLightType(LightType.POINT);scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);HTML5SaveOptions opt = new HTML5SaveOptions();opt.setShowGrid(false); // Turn off the gridopt.setShowUI(false); //Turn off the user interfacescene.save("test.html", FileFormat.HTML5);

### Added new property **FileFormat** in class com.aspose.threed.IOConfig

/\*\* \* Gets the file format that specified in current Save/Load option. \*/public FileFormat getFileFormat();

### Added new method **evaluateGlobalTransform** in class com.aspose.threed.Node

/\*\* \* Evaluate the global transform, include the geometric transform or not. \* @param withGeometricTransform Whether the geometric transform is needed. \*/public Matrix4 evaluateGlobalTransform(boolean withGeometricTransform);

The difference between Node.GlobalTransform.TransformMatrix is that it allows you to get a transformation matrix with a geometric transform, which only affects the attached entity and keeps the child nodes unaffected.

### Added new getter/setter **getGeometricTranslation/setGeometricTranslation/getGeometricScaling/setGeometricScaling/getGeometricRotation/setGeometricRotation** in class com.aspose.threed.Transform

/\*\* \* Gets the geometric translation. \* Geometric transformation only affects the entities attached and leave the child nodes unaffected. \* It will be merged as local transformation when you export the geometric transformation to file types that does not support it. \*/public Vector3 getGeometricTranslation();/\*\* \* Sets the geometric translation. \* Geometric transformation only affects the entities attached and leave the child nodes unaffected. \* It will be merged as local transformation when you export the geometric transformation to file types that does not support it. \* @param value New value \*/public void setGeometricTranslation(Vector3 value);/\*\* \* Gets the geometric scaling. \* Geometric transformation only affects the entities attached and leave the child nodes unaffected. \* It will be merged as local transformation when you export the geometric transformation to file types that does not support it. \*/public Vector3 getGeometricScaling();/\*\* \* Sets the geometric scaling. \* Geometric transformation only affects the entities attached and leave the child nodes unaffected. \* It will be merged as local transformation when you export the geometric transformation to file types that does not support it. \* @param value New value \*/public void setGeometricScaling(Vector3 value);/\*\* \* Gets the geometric euler rotation(measured in degree). \* Geometric transformation only affects the entities attached and leave the child nodes unaffected. \* It will be merged as local transformation when you export the geometric transformation to file types that does not support it. \*/public Vector3 getGeometricRotation();/\*\* \* Sets the geometric euler rotation(measured in degree). \* Geometric transformation only affects the entities attached and leave the child nodes unaffected. \* It will be merged as local transformation when you export the geometric transformation to file types that does not support it. \* @param value New value \*/public void setGeometricRotation(Vector3 value);

Sample code:

Node n = new Node();n.getTransform().setGeometricTranslation(new Vector3(10, 0, 0));System.out.println(n.evaluateGlobalTransform(true));System.out.println(n.evaluateGlobalTransform(false));

The first print statement will output the transform matrix that includes the geometric transformation while the second one will not.  
  

