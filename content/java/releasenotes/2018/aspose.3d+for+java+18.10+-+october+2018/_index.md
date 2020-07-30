---
title : "Aspose.3D for Java 18.10 - October 2018" 
description : "" 
weight : 12076 
toc : false
type: docs
url: /java/releasenotes/2018/aspose.3d+for+java+18.10+-+october+2018/
---

# Aspose.3D for Java : Aspose.3D for Java 18.10 - October 2018


This page contains release notes for [Aspose.3D for Java 18.10](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.10/).

## Improvements and Changes

{{< table style="table-striped" >}}
|Summary|Category|
|:----|:----|
|Support for .NET Core platform|New Feature|
|Allow user to turn off compression when saving FBX binary files|New Feature|
|Improve FBX import performance|Enhancement|
|Improve FBX Binary write performance|Enhancement|
|ImportException while opening huge FBX files|Bug|
|Problem with UnitScaleFactor property|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

Please view the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for Java API. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### API changes:

#### Added members to class Aspose.ThreeD.Formats.FBXSaveOptions:

{{< code lang="cs" >}}
    /**
     * Compression large binary data in the FBX file, default value is true.
     */
    public boolean com.aspose.threed.FBXSaveOptions.getEnableCompression();
    /**
     * Compression large binary data in the FBX file, default value is true.
     */
    public void com.aspose.threed.FBXSaveOptions.setEnableCompression(boolean val);
{{< /code >}}

**Sample Code:**

{{< code lang="cs" >}}
    Scene scene = new Scene("test.fbx");
    FBXSaveOptions opts = new FBXSaveOptions(FileFormat.FBX7500_BINARY);
    opts.setEnableCompression(false);
    scene.save("test.fbx", opts);
{{< /code >}}

