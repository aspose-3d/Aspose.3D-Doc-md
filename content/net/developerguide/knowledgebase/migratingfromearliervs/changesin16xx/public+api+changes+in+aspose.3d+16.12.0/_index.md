---
title : "Public API Changes in Aspose.3D 16.12.0" 
description : "" 
weight : 20078 
toc : false
type: docs
url: /net/developerguide/knowledgebase/migratingfromearliervs/changesin16xx/public+api+changes+in+aspose.3d+16.12.0/
---

# Aspose.3D for .NET : Public API Changes in Aspose.3D 16.12.0


{{< panel title="Contents Summary" style="primary" >}}
*   [Adds Aspose.ThreeD.Metered Class](#adds-aspose.threed.metered-class)
*   [Importing DXF Files](#importing-dxf-files)
{{< /panel >}}
This document describes changes to the Aspose.3D API from version 16.11.0 to 16.12.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

### Adds Aspose.ThreeD.Metered Class

A way to apply a metered license.

**C#**

{{< code lang="c#" >}}
// initialize a metered license class object
Metered metered = new Metered();
// set public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");
//Your other code to use Aspose.3D
{{< /code >}}

### Importing DXF Files

Using the recent version (16.12.0) or higher, developers can import DXF files. The DXF format entry is added for loading purposes.

**C#**

{{< code lang="c#" >}}
// an entry of DXF file in the FileFormat class
public static readonly Aspose.ThreeD.FileFormat DXF;
// load a DXF file
Scene dxfFile = new Scene("wuson.dxf");
{{< /code >}}

