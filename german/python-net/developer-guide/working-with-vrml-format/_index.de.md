---
title: Arbeiten mit dem VRML-Format
type: docs
weight: 120
url: /de/python-net/working-with-vrml-format/
description: Aspose.3D for Python via .NET ermöglicht die Arbeit mit VRML Version 1.0. Das Dateiformat VRML wurde der FileFormat-Klasse hinzugefügt. Aspose.3D kann das Format automatisch erkennen, sodass das File Format in der Open-Methode normaler weise ignoriert wird. Das folgende Code-Snippet zeigt, wie öffnen VRML Dateiformat.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.4 oder höher unterstützt.

{{% /alert %}} 
#  **Öffnen Sie VRML-Dateiformat**
Aspose.3D for Python via .NET ermöglicht die Arbeit mit VRML Version 1.0. Das Dateiformat `VRML` wurde der Klasse `FileFormat` hinzugefügt. Aspose.3D kann das Format automatisch erkennen, sodass die `FileFormat` in der `open`-Methode normaler weise ignoriert wird. Das folgende Code-Snippet zeigt, wie öffnen VRML Dateiformat.

{{< highlight "python" >}}
from aspose.threed import Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Open Virtual Reality Modeling Language (VRML) file format
scene.open("data-dir"  + "test.wrl")

{{< /highlight >}}
