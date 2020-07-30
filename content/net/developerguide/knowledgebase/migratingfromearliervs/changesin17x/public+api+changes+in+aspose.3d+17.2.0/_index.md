---
title : "Public API Changes in Aspose.3D 17.2.0" 
description : "" 
weight : 20075 
toc : false
type: docs
url: /net/developerguide/knowledgebase/migratingfromearliervs/changesin17x/public+api+changes+in+aspose.3d+17.2.0/
---

# Aspose.3D for .NET : Public API Changes in Aspose.3D 17.2.0


{{< panel title="Contents Summary" style="primary" >}}
*   [Importing DirectX X Files](#importing-directx-x-files)
*   [Adds Aspose.ThreeD.Formats.X.XLoadOptions Class](#adds-aspose.threed.formats.x.xloadoptions-class)
{{< /panel >}}
This document describes changes to the Aspose.3D API from version 17.1.0 to 17.2.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

#### Importing DirectX X Files

Using the recent version (17.02) or higher, developers can import X files. The XBinary and XText format entries are added to import binary and ASCII X files.

**C#**

{{< code lang="c#" >}}
// XBinary and XText entries are added in the FileFormat class
public static readonly Aspose.ThreeD.FileFormat XBinary;
public static readonly Aspose.ThreeD.FileFormat XText;

// load X file
Scene Xfile = new Scene("3D.x");
{{< /code >}}

#### Adds Aspose.ThreeD.Formats.X.XLoadOptions Class

We have added `XLoadOptions` class. It helps in importing X files into Aspose.3D API.

**C#**

{{< code lang="c#" >}}
// XBinary and XText entries are added in the FileFormat class
public static readonly Aspose.ThreeD.FileFormat XBinary;
public static readonly Aspose.ThreeD.FileFormat XText;
// initialize Scene class object
Scene scene = new Scene();
// initialize an object
XLoadOptions loadXOpts = new XLoadOptions();
// load X file
scene.Open( "3DX.x", loadXOpts);
{{< /code >}}

