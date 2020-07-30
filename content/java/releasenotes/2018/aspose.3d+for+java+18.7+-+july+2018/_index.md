---
title : "Aspose.3D for Java 18.7 - July 2018" 
description : "" 
weight : 12079 
toc : false
type: docs
url: /java/releasenotes/2018/aspose.3d+for+java+18.7+-+july+2018/
---

# Aspose.3D for Java : Aspose.3D for Java 18.7 - July 2018


This page contains release notes for [Aspose.3D for Java 18.7](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.7/).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Summary|Category|
|:----|:----|
|Add Draco 2.2 import support|New Feature|
|Add Draco 2.2 export support|New Feature|
|Import glTF files with draco compression|New Feature|
{{< /table >}}

### Public API and Backwards Incompatible Changes

Please view the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java API. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### API changes:

#### 3 members removed from class com.aspose.threed.Property:

{{< code lang="cs" >}}
    public void com.aspose.threed.Property.setExtraData(java.lang.String);
    public java.lang.String com.aspose.threed.Property.getExtraData();
    public int com.aspose.threed.Property.getFlags();
{{< /code >}}

These are removed to synchronize the changes from .NET version. (They are scheduled to be removed since Aspose.3D for .NET 18.2)

#### 1 property added to class com.aspose.threed.ObjLoadOptions:

{{< code lang="cs" >}}
    public boolean com.aspose.threed.ObjLoadOptions.getNormalizeNormal();
    public void com.aspose.threed.ObjLoadOptions.setNormalizeNormal(boolean);
{{< /code >}}

Gets or sets whether to normalize the normal vector during the loading, default value is true.

##### Sample code:

{{< code lang="cs" >}}
        Scene scene = new Scene();
        ObjLoadOptions opt = new ObjLoadOptions();
        opt.setNormalizeNormal(false);
        scene.open("test.obj", opt);
{{< /code >}}

This will load the obj file and leave the normal vectors unnormalized, the old version will normalize the normal vectors when obj file loaded.

