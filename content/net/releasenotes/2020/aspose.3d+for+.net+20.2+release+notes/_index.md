---
title : "Aspose.3D for .NET 20.2 Release Notes" 
description : "" 
weight : 12098 
toc : false
type: docs
url: /net/releasenotes/2020/aspose.3d+for+.net+20.2+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 20.2 Release Notes


This page contains release notes information for Aspose.3D for .NET 20.2

## Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-612 | IFC compatible procedural I shape generation | New feature |
|THREEDNET-615 | IFC compatible procedural C shape generation | New feature |
|THREEDNET-616 | IFC compatible procedural Z shape generation | New feature |
|THREEDNET-617 | IFC compatible procedural L shape generation | New feature |
|THREEDNET-618 | IFC compatible procedural T shape generation | New feature |
|THREEDNET-619 | IFC compatible procedural U shape generation | New feature |
|THREEDNET-620 | IFC compatible procedural rectangle shape generation | New feature |
|THREEDNET-625 | IFC compatible procedural circle shape generation | New feature |
|THREEDNET-626 | IFC compatible procedural ellipse shape generation | New feature|
|THREEDNET-558 | Add transparency rendering support in web renderer | Enhancement |
|THREEDNET-606 | Display bounding box if node selected in Asset browser. | Enhancement |
|THREEDNET-613 | Add the rendering support of shape | Enhancement |
|THREEDNET-630 | Process hangs when loading RVM files | Bug |
|THREEDNET-632 | Exception on loading FBX file | Bug |
|THREEDNET-629 | Exception on converting GLB to 3d | Bug |
|THREEDNET-623 | Intel's GPU is not supported by the Aspose.3D renderer | Bug |
|THREEDNET-628 | Exception on loading FBX file | Bug |
{{< /table >}}

## Public API and Backward Incompatible Changes

### Added new class **Aspose.ThreeD.Profiles.Profile**

This class is the base class of all profiles, which can be used to create parameterized meshes. A Profile class represents a 2D profile in x-y plane.

{{< code lang="cs" >}}
    /// <summary>
    /// 2D Profile in xy plane
    /// </summary>
    public abstract class Profile : Entity
    {
        /// <summary>
        /// Gets the extent in x and y dimension.
        /// </summary>
        /// <returns></returns>
        public abstract Vector2 GetExtent();
    }
    /// <summary>
    /// The base class of all parameterized profiles.
    /// </summary>
    public abstract class ParameterizedProfile : Profile
    {
    }
{{< /code >}}

All the subclass of Profile can be converted to 3D mesh through LinearExtrusion as shown in the following sample code:

{{< code lang="cs" >}}
var mesh = new LinearExtrusion(new LShape()
    {
     FilletRadius = 1,
     Width = 4,
     Depth = 7
      }, 1);
Scene s = new Scene(mesh);
s.Save(@"LShape.obj", FileFormat.WavefrontOBJ);
{{< /code >}}

### Added new class **Aspose.ThreeD.Profiles.CircleShape**

Properties of CircleShape can be illustrated in the figure below.

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089370.png)

### Added new class **Aspose.ThreeD.Profiles.CShape**

Properties of CShape can be illustrated in the figure below:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089371.png)

### Added new class **Aspose.ThreeD.Profiles.EllipseShape**

Properties of EllipseShape can be illustrated in this figure:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089372.png)

### Added new class **Aspose.ThreeD.Profiles.HShape**

Properties of HShape can be illustrated in this figure:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089373.png)

### Added new class **Aspose.ThreeD.Profiles.LShape**

Properties of LShape can be illustrated in this figure:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089374.png)

### Added new class **Aspose.ThreeD.Profiles.RectangleShape**

Properties of RectangleShape can be illustrated in this figure:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089375.png)

### Added new class **Aspose.ThreeD.Profiles.TrapeziumShape**

Properties of TrapeziumShape can be illustrated in this figure:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089376.png)

### Added new class **Aspose.ThreeD.Profiles.TShape**

Properties of TShape can be illustrated in the figure below:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089377.png)

### Added new class **Aspose.ThreeD.Profiles.UShape**

Properties of UShape can be illustrated in the following figure:

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089378.png)

### Added new class **Aspose.ThreeD.Profiles.ZShape**

Properties of ZShape can be illustrated in the following figure.

![](https://docs2.aspose.com/3d/net/attachments/101122868/101089379.png)

### Added new class **Aspose.ThreeD.Profiles.MirroredShape**

This profile defines a new profile by mirroring the base profile about the y-axis.

{{< code lang="cs" >}}
var mesh = new LinearExtrusion(new MirroredProfile(new LShape()
            {
                FilletRadius = 1,
                Width = 4,
                Depth = 7
            }), 1);
Scene s = new Scene(mesh);
s.Save(@"MirroredLShape.obj", FileFormat.WavefrontOBJ);
{{< /code >}}

  

