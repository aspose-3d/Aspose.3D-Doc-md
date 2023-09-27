---
title: Aspose.3D for Python via .NET 23.9 Release Notes
type: docs
weight: 4
url: /python-net/aspose-3d-for-python-net-23-9-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes information for Aspose.3D for Python via .NET 23.9.

{{% /alert %}}
## **Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
| THREEDNET-1430 | Prepare migration to System.Numerics | Task |
| THREEDAPP-2055 | Watermark may not working for some meshes | Bug fixing |
| THREEDAPP-2065 | Conversion issue  | Bug fixing |
| THREEDAPP-2066 | Bump texture lost when fbx is converted to obj | Bug fixing |
| THREEDNET-1429 | Mesh triangulation may fail sometimes | Bug fixing |


### API Changes

### Added members to class **aspose.threed.utilities.BoundingBox**:

{{< highlight python >}}

        # Calculates the absolute largest coordinate value of any contained point.
        def scale()

        # Merge current bounding box with given point
        def merge(pt)

        # Merge current bounding box with given point
        def merge(x, y, z)

        # Check if current bounding box overlaps with specified bounding box. 
        def merge(bb)

        # Check if current bounding box overlaps with specified bounding box. 
        def overlaps_with(box)

        # Check if the point p is inside the bounding box
        def contains(pt)
{{</highlight>}}

