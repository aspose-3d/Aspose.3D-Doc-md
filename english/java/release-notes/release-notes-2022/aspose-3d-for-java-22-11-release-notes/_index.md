---
title: Aspose.3D for Java 22.11 Release Notes
type: docs
weight: 2
url: /java/aspose-3d-for-java-22-11-release-notes/
description: The release notes of Aspose.3D for Java 22.11.
---

{{% alert color="primary" %}}

This page contains release notes information for Aspose.3D for Java 22.11.

{{% /alert %}}
## **Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
| THREEDNET-1283 | Implement binary maya import support | New Feature |
| THREEDNET-1276 | Improve mesh quality when converting 3D-PDF to GLTF | Improvement |
| THREEDNET-1280 | Restore the support of .NET 4.5 | Improvement |
| THREEDNET-1289 | Materials lost when export to USDZ with only diffuse colors | Bug fix |
| THREEDJAVA-227 | Stl to obj in java | Bug fix |

## API changes ##

### Added members to class `com.aspose.threed.FileFormat`:


{{< highlight java >}}

    /**
     * Autodesk Maya in Binary format
     */
    public static final FileFormat MAYA_BINARY;

{{< /highlight >}}

Aspose.3D supports Maya binary format as input format.

