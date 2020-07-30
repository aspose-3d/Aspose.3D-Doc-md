---
title : "Aspose.3D for Java 18.8 - August 2018" 
description : "" 
weight : 12078 
toc : false
type: docs
url: /java/releasenotes/2018/aspose.3d+for+java+18.8+-+august+2018/
---

# Aspose.3D for Java : Aspose.3D for Java 18.8 - August 2018


This page contains release notes for [Aspose.3D for Java 18.8](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.8/).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Summary|Category|
|:----|:----|
|Export glTF files with draco compression|New Feature|
|Optimize memory consumption for mesh indices|Enhancement|
|Use Aspose.3D with Unity3D|Bug|
|Read COLLADA files referencing in same folder|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

Please view the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java API. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### API changes:

#### Added a new getter/setter to class com.aspose.threed.GLTFSaveOptions:

{{< code lang="cs" >}}
        public bool getDracoCompression();
        public void setDracoCompression(boolean value);
{{< /code >}}

The default value is true, when this is enabled by setting to true, the glTF 2.0 exporter will encode the mesh in Google Draco format.

